<div class="flex py-3 text-white font-aileron font-extrabold text-2xl overflow-clip">
    <div class="breadcrumb bg-uninteresting-yellow relative -left-30"></div>
    <div class="breadcrumb bg-funky-orange relative -left-36">Consulting</div>
    <div class="breadcrumb bg-royal-blue relative -left-45">Research</div>
    <div class="breadcrumb bg-too-red relative -left-54">Publications</div>
    <div class="breadcrumb bg-uninteresting-yellow relative -left-63"></div>
</div>

<style>
    .breadcrumb {
        --s: 120px;
        line-height: 9;
        padding-inline: calc(var(--s) + .3em);
        clip-path: polygon(0 0,calc(100% - var(--s)) 0,100% 50%,calc(100% - var(--s)) 100%,0 100%,var(--s) 50%);
        width: 480px;
    }
</style>