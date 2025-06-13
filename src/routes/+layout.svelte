<script>
	import '../app.css';

	let { children } = $props();

    const routes = ['collaborations', 'publications', 'research']; 
    
    let y = $state(0);
    
</script>

<svelte:window bind:scrollY={y}/>

<nav class="flex justify-between px-10 bg-off-white border-b-2 border-uninteresting-yellow sticky top-0 z-100">
    <a href="/" class="p-4 text-2xl text-too-red font-anton font-bold">ICON</a>
    <div class="flex">
    {#each routes as route}
        <a href="\{route}" class="p-4 text-xl text-funky-orange font-tt-hoves font-bold text-center hover:text-royal-blue">{route.charAt(0).toUpperCase() + route.slice(1)}</a>
    {/each}
	</div>
</nav>

{@render children()}