<script>
	import { ProjectCard } from '$lib/components';
	export let data;
</script>

<body>
	<title>Home</title>
	<div class="flex flex-col gap-3">
		<h1 class="text-2xl font-bold">Projects made by others</h1>
		<p class="font-xs italic">They may also include your own.</p>

		<div class="grid grid-cols-3 gap-2">
			{#each data.projects as project}
				<ProjectCard {project} />
			{/each}
		</div>
	</div>
	<br />
	<footer>
		<a class="btn btn-primary flex m-14" href="/contact-us">contact us</a>
	</footer>

	<style>
		footer {
			border-top: 3px;
			border-style: solid;
			border-color: rgb(115, 115, 115);
		}
	</style>
</body>
