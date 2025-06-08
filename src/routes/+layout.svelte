<script>
	import '../app.css';

	let { children } = $props();

    const routes = ['collaborations', 'publications', 'research']; 
</script>

<nav class="flex justify-between mx-10 border-b-2 border-uninteresting-yellow">
    <a href="/" class="p-4 text-2xl text-too-red font-anton font-bold">ICON</a>
    <div class="flex">
    {#each routes as route}
        <a href="\{route}" class="p-4 text-xl text-funky-orange font-tt-hoves font-bold text-center">{route.charAt(0).toUpperCase() + route.slice(1)}</a>
    {/each}
	</div>
</nav>

{@render children()}