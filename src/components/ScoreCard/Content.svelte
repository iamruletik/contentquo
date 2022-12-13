<script>
	const by_severities = '/images/by_severities.png';
	const by_category = '/images/by_category.png';
	import Comments from './Comments.svelte';
	import UiDropdown from '../UiDropdown.svelte';
	import DashbBlock from '../DashbBlock.svelte';
</script>

<main>
	<div class="bg-amber-500 flex gap-1">
		<div class="bg-blue-200 min-w-min max-w-600 pl-12">Translated by</div>
		<div class="bg-orange-200 min-w-min">Source Words</div>
		<div class="bg-green-200 min-w-min">Segments</div>
		<div class="bg-yellow-200 grow">Workflow & Quality Profile</div>
	</div>
	<qualityscore class="ml-12 flex gap-3 items-start">
		<div class=" min-w-min flex flex-col border px-3 py-4 border-slate-200">
			<div>Analytical Score</div>
			<div class="flex items-baseline">
				<div class="text-4xl">76% Fail</div>
				<div class="text-sm">of 3.0</div>
			</div>
		</div>
		<div class="grow max-w-sm min-h-min border px-3 py-4 border-slate-200">
			<div>4 issues by severities</div>
			<img class="fit-picture" src={by_severities} alt="4 issues by severities" />
		</div>
		<div class="bg-green-200 min-h-min   max-w-sm border px-3 py-4 border-slate-200">
			<div>Issues by category</div>
			<img class="fit-picture" src={by_category} alt="4 issues by severities" />
		</div>
		<div class="bg-yellow-200 min-w-min border px-3 py-4 border-slate-200">
			<div>Edit Distance</div>
			<div class="text-4xl">2</div>
			<hr />
			<div>>5</div>
			<div>segments edited</div>
		</div>
	</qualityscore>

	<comments class="ml-12 grid grid-flow-row pt-16">
		<h2 class="text-2xl pb-4">Overall comment <i class="fa fa-commenting text-amber-300" /></h2>
		<comment_row class="grid grid-cols-2 grid-flow-row gap-8 p-y-8 mb-10">
			<div class=""><Comments /></div>
			<div class=""><Comments /></div>
			<div class=""><Comments /></div>
			<div class=""><Comments /></div>
		</comment_row>
		<comment_row class="grid grid-cols-2 grid-flow-row gap-8 p-y-8 mb-10">
			<div class=""><Comments /></div>
			<div class=""><Comments /></div>
			<div class=""><Comments /></div>
		</comment_row>
		<comment_row class=" grid grid-cols-2 grid-flow-row gap-4 mb-10">
			<div class=""><Comments /></div>
			<div class=""><Comments /></div>
		</comment_row>
		<comment_row class="grid grid-cols-2 grid-flow-row gap-8 p-y-8 mb-10">
			<div class=""><Comments /></div>
		</comment_row>
		<comment_row class="grid grid-cols-2 grid-flow-row gap-8 p-y-8 mb-10">
			<div class="text-xs">No comments</div>
		</comment_row>
	</comments>
	<mainscorecardgraphsbig class="grid grid-rows-1 gap-6 ml-12 pt-8">
		<div class="flex gap-2">
			<UiDropdown butontext="All data" />
			<UiDropdown butontext="Filters" />
		</div>
		<div class="grid grid-rows-1 gap-6 ">
			<DashbBlock
				dashb_title="Holistic Issues Distribution"
				dashb_subtitle1="% of segments"
				dashb_subtitle2="% of words"
				dashb_img="/images/Average-rating-per-segment-weighted-by-segment-length.jpg"
			/>
			<DashbBlock
				dashb_title="Analytical Issues Distribution"
				dashb_subtitle1="% of segments"
				dashb_subtitle2="% of words"
				dashb_img="/images/Analytical Issues Distribution.jpg"
			/>
			<DashbBlock
				dashb_title="Analytical Quality"
				dashb_subtitle1="Issues:"
				dashb_subtitle2="3 in 3 categories"
				dashb_img="/images/Analytical Quality.jpg"
			/>
			<DashbBlock
				dashb_title="Holistic Issues Distribution"
				dashb_subtitle1="% of segments"
				dashb_subtitle2="% of words"
				dashb_img="/images/Holistic Issues Distribution.jpg"
			/>
			<div>
				<h2 class="text-2xl pb-4 pt-8">Text, average rating per %</h2>
				<avratpertext class="grid grid-cols-3 gap-4">
					<DashbBlock
						dashb_title="Linguist #1"
						dashb_subtitle1=" "
						dashb_subtitle2=" "
						dashb_img="/images/Linguist-1.jpg"
					/>
					<DashbBlock
						dashb_title="Linguist #2"
						dashb_subtitle1=" "
						dashb_subtitle2=" "
						dashb_img="/images/Linguist-2.jpg"
					/>
					<DashbBlock
						dashb_title="Overall"
						dashb_subtitle1=" "
						dashb_subtitle2=" "
						dashb_img="/images/Overall.jpg"
					/>
				</avratpertext>
				<h2 class="text-2xl pb-4 pt-8">Segments, average rating per %</h2>
				<avratperseg class="grid grid-cols-3 gap-4"
					><DashbBlock
						dashb_title="Linguist #1"
						dashb_subtitle1=" "
						dashb_subtitle2=" "
						dashb_img="/images/Linguist-1.jpg"
					/>
					<DashbBlock
						dashb_title="Linguist #2"
						dashb_subtitle1=" "
						dashb_subtitle2=" "
						dashb_img="/images/Linguist-2.jpg"
					/>
					<DashbBlock
						dashb_title="Overall"
						dashb_subtitle1=" "
						dashb_subtitle2=" "
						dashb_img="/images/Overall.jpg"
					/>
				</avratperseg>

				<h2 class="text-2xl pb-4 pt-8">Holistic score per segment length, average</h2>
				<holscoreseg class="grid grid-cols-2 gap-4">
					<DashbBlock
						dashb_title="Linguist #1"
						dashb_subtitle1=" "
						dashb_subtitle2=" "
						dashb_img="/images/Linguist-1.jpg"
					/>
					<DashbBlock
						dashb_title="Linguist #2"
						dashb_subtitle1=" "
						dashb_subtitle2=" "
						dashb_img="/images/Linguist-2.jpg"
					/>
				</holscoreseg>
				<holscoreoverall class="grid grid-cols-1 gap-4">
					<DashbBlock
						dashb_title="Overall"
						dashb_subtitle1=" "
						dashb_subtitle2=" "
						dashb_img="/images/Overall.jpg"
					/></holscoreoverall
				>

				<h2 class="text-2xl pb-4 pt-8">Similarity between linguists, %</h2>

				<DashbBlock
					dashb_title="Average rating per segment weighted by segment length"
					dashb_subtitle1=" "
					dashb_subtitle2=" "
					dashb_img="/images/Average rating per segment weighted by segment length.jpg"
				/>
			</div>
		</div>
	</mainscorecardgraphsbig>
</main>
