<script>
	//const companyLogo = new URL("/images/test_logo.jpg", import.meta.url).href
	const companyLogo = '/images/test_logo.jpg';
	let companyName = 'Keywords Studios';
	import SearchInput from '../components/SearchInput.svelte';
</script>

<section class="bg-slate-100 h-screen w-56 border-slate-200 border-r-2 box-border static">
	<div
		id="companyId"
		class="w-full h-auto py-3 px-4 flex items-center hover:bg-slate-200 active:bg-slate-300 transition cursor-pointer group"
	>
		<div
			id="companyLogo"
			class="w-8 h-8 border-2  border-slate-200 box-border rounded-lg group-hover:shadow-md group-hover:border-slate-300 transition"
		>
			<img class="rounded-lg" src={companyLogo} alt="Company Name" />
		</div>

		<h6 class="font-semibold text-base ml-2 text-slate-900">{companyName}</h6>
	</div>

	<div id="searchInput" class="w-full px-4 pt-1 pb-4">
		<SearchInput />
	</div>
</section>
