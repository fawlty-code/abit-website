<script>
    import deco from '$lib/assets/deco-bg.png';
    import arches from '$lib/assets/arches.png';
    import leaves from '$lib/assets/too-red-leaves.png';
    import smallarch from '$lib/assets/uninteresting-yellow-arch.png';
    import circle from '$lib/assets/funky-orange-circle.png';
    import star from '$lib/assets/royal-blue-star.png';
    import consuma from '$lib/assets/consuma-logo.png';
    import iben from '$lib/assets/iben-logo.png';
    import infoedge from '$lib/assets/infoedge-logo.png';
    import rockethealth from '$lib/assets/rocket-health-logo.png';
    import csbc from '$lib/assets/csbc-logo.png';
    import stories from '$lib/assets/1001-stories-logo.jpg';
    import Boxset from '$lib/boxset.svelte';
    import Breadcrumbs from '$lib/breadcrumbs.svelte';
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
        <Boxset></Boxset>
        <div class="bg-uninteresting-yellow mx-3 text-uninteresting-yellow flex-auto w-6"></div>
    </div>
    <div>
        <div class="py-2 text-5xl text-funky-orange font-tt-hoves font-bold">Recent Events</div>
        <div class="text-slate-gray font-aileron text-lg pl-0.5 py-2">
            <a href="https://sites.google.com/view/brewindia/brew-esa-2024"><b><u>Behavioural Research in Economics Workshop</u></b></a><br>
            BREW, hosted by Ashoka University and Centre for Social and Behaviour Change, was a 3-day conference with 84 behavioural scientists and presenters from around the world, making it the largest BREW yet! <br><br>ABIT helped with event logistics, student poster presentations alongside a fantastic team of student volunteers. 11 students from Psychology and Economics showcased their research ranging from topics like common pool resources and substance use among Tibetan youth.
        </div>
    </div>
    <div class="grid grid-cols-4 my-4 ml-2 pl-2 bg-gradient-to-r from-grad-pink via-grad-magenta to-grad-indigo border-hidden rounded-l-full">
        <button class="col-start-1 row-auto text-3xl text-white">⫷</button>
        <img class="col-span-2 py-12" src={deco} alt="alt text">
        <button class="col-start-4 row-auto text-3xl text-white">⫸</button>
    </div>
</div>

<div class="flex justify-between">
    <span class="bg-slate-gray font-anton text-off-white font-extrabold text-6xl p-3 rounded-3xl">
        BEHAVIOURAL SCIENCES
    </span>

    <div class="flex flex-row p-4.5">
        <div class="m-7.5">
        </div>
        <div class="grid grid-cols-6 grid-rows-6 pr-6 gap-1.5 text-off-white text-xl font-semibold font-tt-hoves">
            <div class="flex bg-slate-gray p-3 rounded-2xl row-start-1 row-span-3 col-start-2 col-span-2">
                <img src={leaves} alt="leaves" height="100" width="100">
                <span>What is it?</span>
            </div>
            <div class="flex bg-slate-gray p-3 rounded-2xl row-start-2 row-span-2 col-start-4 col-span-3">
                <span>Why do we need it?</span>
                <img src={circle} alt="circle" height="100" width="100">
            </div>
            <div class="flex bg-slate-gray p-3 rounded-2xl row-start-4 row-span-3 col-start-4 col-span-2">
                <img src={star} alt="star" height="100" width="100">
                <span>What is the scope for the future?</span>
            </div>
            <div class="flex bg-slate-gray p-3 rounded-2xl row-start-4 row-span-2 col-start-1 col-span-3">
                <img src={smallarch} alt="arch" height="100" width="100">
                <span>How does ABIT contribute to it?</span>
            </div>
        </div>
    </div>
</div>

<div class="px-4 flex">
    <Boxset></Boxset>
    <div class="px-4.5 self-center text-5xl text-royal-blue font-tt-hoves font-bold">What We Do?</div>
</div>
<Breadcrumbs></Breadcrumbs>

<div class="flex">
    <div class="px-4 py-2 flex flex-col gap-4 flex-none">
        <Boxset></Boxset>
        <div class="bg-uninteresting-yellow mx-3 text-uninteresting-yellow flex-auto w-6"></div>
    </div>
    <div class="relative -bottom-21">
        <div class="py-2 text-5xl text-too-red font-tt-hoves font-bold">Partners</div>
        <div class="grid gap-3 py-3 grid-cols-6">
            <img src={consuma} alt="consuma-logo" class="self-center col-start-1 col-span-2">
            <img src={csbc} alt="csbc-logo" class="self-center col-start-4 col-span-2">
            <img src={rockethealth} alt="rocket-health-logo" class="self-center col-start-2 col-span-2">
            <img src={infoedge} alt="infoedge-logo" class="self-center col-start-5 col-span-2">            
            <img src={iben} alt="iben-logo" class="self-center col-span-2">
            <img src={stories} alt="1001-stories-logo" class="self-center col-start-4 col-span-2">
        </div>
    </div>
    <img src={arches} alt="arches" class="pl-3">
</div>