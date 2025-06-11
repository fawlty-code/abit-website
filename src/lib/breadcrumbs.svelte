<div class="flex text-white font-aileron font-extrabold text-2xl overflow-clip">
    <div class="breadcrumb bg-uninteresting-yellow relative -left-24"></div>
    <div class="breadcrumb bg-funky-orange">Consulting</div>
    <div class="breadcrumb bg-royal-blue">Research</div>
    <div class="breadcrumb bg-too-red">Publications</div>
    <div class="breadcrumb bg-uninteresting-yellow"></div>
</div>

<style>
    .breadcrumb {
        --s: 90px;
        line-height: 6;
        padding-inline: calc(var(--s) + .3em);
        clip-path: polygon(0 0,calc(100% - var(--s)) 0,100% 50%,calc(100% - var(--s)) 100%,0 100%,var(--s) 50%);
        width: 360px;
    }
</style>
