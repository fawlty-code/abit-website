<script>
    import deco from '$lib/assets/deco-bg.png';
    let colors = ['funky-orange','royal-blue','too-red'];
</script>

<div class="grid grid-cols-3 p-2">
    <div class="p-4 pl-12 col-span-1 text-6xl text-too-red font-anton font-bold">ASHOKA BEHAVIOURAL INSIGHTS TEAM</div>
    <div class="relative pl-12 row-start-2">
        <div class="absolute -top-18 text-xl text-royal-blue font-tt-hoves font-extrabold">Striving to drive<br>impactful change</div>
    </div>
    <div class="p-4 px-12 col-span-2 row-span-auto">
        <p class="text-slate-gray font-aileron text-lg font-semibold">The Ashoka Students Behavioural Insights Team (ABIT) is <b>India’s first student-led behavioural insights team</b>, operating out of Ashoka University, affiliated and funded by the <b>Centre for Social and Behaviour Change (CSBC)</b>. <br><br>We study all things B-Sci - policy, well-being, pop culture, consumer behaviour, organisational structures, business design and pretty much anything else under the sun. As a student-led organisation, we aim to explore and apply the many facets of behavioural science and interdisciplinary research to our every-day surroundings, and drive impactful change!</p>
    </div>
</div>

<div class="grid grid-cols-2">
    <img src={deco} alt="80s deco background" class="col-start-1 row-start-1 col-span-2 p-8 pr-36">
    <div class="grid grid-rows-4 px-12">

    </div>
    <div class="grid grid-rows-2 px-12 gap-36">

    </div>
</div>

<div class="flex">
    <div class="px-4 py-2 flex flex-col gap-4 flex-none">
        {#each colors as color}
            <div class="bg-{color} min-h-4 min-w-4 p-1.5 text-{color}">ab</div>
        {/each}
        <div class="bg-uninteresting-yellow m-1.5 text-uninteresting-yellow flex-auto">abc</div>
    </div>
    <div>
        <div class="text-5xl text-funky-orange font-tt-hoves font-bold">Recent Events</div>
        <div class="text-slate-gray font-aileron text-lg pl-0.5 py-2">
            <a href="https://sites.google.com/view/brewindia/brew-esa-2024"><b><u>Behavioural Research in Economics Workshop</u></b></a><br>
            BREW, hosted by Ashoka University and Centre for Social and Behaviour Change, was a 3-day conference with 84 behavioural scientists and presenters from around the world, making it the largest BREW yet! <br><br>ABIT helped with event logistics, student poster presentations alongside a fantastic team of student volunteers. 11 students from Psychology and Economics showcased their research ranging from topics like common pool resources and substance use among Tibetan youth.
        </div>
    </div>
    <div class="grid grid-cols-4 pl-4">
        
    </div>
</div>