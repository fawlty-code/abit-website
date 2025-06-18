<script>
    let { trailing } = $props();
</script>

<div class="px-4 py-2.5 flex flex-col flex-none">
    <div class="m-1 p-4.5 w-4.5 h-4.5 bg-funky-orange"></div>
    <div class="m-1 p-4.5 w-4.5 h-4.5 bg-royal-blue"></div>
    <div class="m-1 p-4.5 w-4.5 h-4.5 bg-too-red"></div>
    {#if trailing}
    <div class="bg-uninteresting-yellow my-1 mx-3 flex-auto w-5"></div>
    {/if}
</div>