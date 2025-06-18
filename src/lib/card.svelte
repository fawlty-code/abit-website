<script>
    let { gridProps, imageSrc, cardTitle, cardText, imageProps, imageSize, titleProps } = $props();
</script>

<article class="group {gridProps} h-80 max-w-80 bg-transparent perspective-midrange">
    <div class="relative h-full w-full text-center transition-transform duration-500 transform-3d group-hover:rotate-y-180">
    <section class="absolute flex justify-between h-full w-full rounded-2xl bg-off-white p-3 text-slate-gray text-2xl font-bold font-tt-hoves backface-hidden">
        <img src={imageSrc} alt="leaves" height={imageSize} width={imageSize} class="{imageProps}">
        <span class="{titleProps} py-3 px-3">{cardTitle}</span>
    </section>
    <section class="absolute flex h-full w-full rotate-y-180 flex-col rounded-2xl justify-center bg-slate-gray p-3 text-off-white backface-hidden">
        <p>{cardText}</p>
    </section>
    </div>
</article>