<script>
    import au1 from '$lib/assets/au-1.jpg';
    import au2 from '$lib/assets/au-2.jpg';
    import au3 from '$lib/assets/au-3.jpg';

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

    import event1 from '$lib/assets/event_1.png';
    import event2 from '$lib/assets/event_2.png';
    import event3 from '$lib/assets/event_3.png';
    import event4 from '$lib/assets/event_4.png';
    import event5 from '$lib/assets/event_5.png';
    import event6 from '$lib/assets/event_6.png';
    
    let index = $state(0);
    const images = [event1, event2, event3, event4, event5, event6];
    function changeImage(i) {
        index = (index + i + images.length) % images.length;
    }

    import { fly } from 'svelte/transition';
    
    let eventVisible = $state(false);
    let whatwedoVisible = $state(false);
    let partnersVisible = $state(false);

    function inView(node, k) {
        const observer = new IntersectionObserver(([entry]) => {
            if (entry.isIntersecting) {
                if(k==1) {
                    eventVisible = true;
                }
                else if(k==2) {
                    whatwedoVisible = true;
                }
                else if(k==3) {
                    partnersVisible = true;
                }
                observer.unobserve(node);
            }
        }, { threshold: 0.1 });

        observer.observe(node);

        return {
            destroy() {
            observer.disconnect();
            }
        };
    }
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

<div class="grid grid-cols-2 grid-rows-2 bg-[url('$lib/assets/deco-bg.png')] bg-center bg-no-repeat bg-contain">
    <img src={au1} alt="Ashoka University 1" class="col-start-1 row-start-1 row-span-2 self-center p-12">
    <img src={au2} alt="Ashoka University 2" class="col-start-2 row-start-1 row-span-1 px-12 py-9">
    <img src={au3} alt="Ashoka University 3" class="col-start-2 row-start-2 row-span-1 px-12 py-9">
</div>

<div class="flex">
    <div class="px-4 py-2 flex flex-col gap-4 flex-none">
        <Boxset></Boxset>
        <div class="bg-uninteresting-yellow mx-3 text-uninteresting-yellow flex-auto w-6"></div>
    </div>
    <div use:inView={1}>
        {#if eventVisible}
        <div class="py-2 text-5xl text-funky-orange font-tt-hoves font-bold" transition:fly={{y:25, duration:1000}}>Recent Events</div>
        {:else}
        <div class="py-2 text-5xl text-funky-orange font-tt-hoves font-bold opacity-0">Recent Events</div>
        {/if}
        <div class="text-slate-gray font-aileron text-lg pl-0.5 py-2">
            <a href="https://sites.google.com/view/brewindia/brew-esa-2024"><b><u>Behavioural Research in Economics Workshop</u></b></a><br>
            BREW, hosted by Ashoka University and Centre for Social and Behaviour Change, was a 3-day conference with 84 behavioural scientists and presenters from around the world, making it the largest BREW yet! <br><br>ABIT helped with event logistics, student poster presentations alongside a fantastic team of student volunteers. 11 students from Psychology and Economics showcased their research ranging from topics like common pool resources and substance use among Tibetan youth.
        </div>
    </div>
    <div class="grid grid-cols-4 grid-rows-1 my-4 ml-2 pl-2 bg-gradient-to-r from-grad-pink via-grad-magenta to-grad-indigo border-hidden rounded-l-full">
        <button onclick={(event) => {changeImage(1)}} class="col-start-1 row-auto text-3xl text-white">⫷</button>
        {#each images as img, i}
        <img class="col-start-2 col-span-2 row-start-1 self-center py-12 transition-opacity duration-500 {index === i ? 'opacity-100' : 'opacity-0'}" src={img} alt={`Event ${i + 1}`} loading="{index === 1 ? 'eager' : 'lazy'}">
        {/each}
        <button onclick={(event) => {changeImage(-1)}} class="col-start-4 row-auto text-3xl text-white h-full">⫸</button>
    </div>
</div>

<div class="flex justify-between my-9">
    <span class="bg-slate-gray w-xs font-dreamwalker text-off-white text-center font-extrabold text-7xl p-3 rounded-r-2xl content-center" style="writing-mode: vertical-lr;">
        BEHAVIOURAL SCIENCES
    </span>
    <div class="flex flex-col items-center">
        <svg class="py-9" xmlns="http://www.w3.org/2000/svg" width="250" viewBox="0 0 48 48"><path fill="none" stroke="#000000" stroke-linecap="round" stroke-linejoin="round" d="M29.428 20.476a3.77 3.77 0 0 1 2.029-2.173a4.12 4.12 0 0 1 3.066-.11c2.098.744 3.219 2.973 2.503 4.979c-.358 1.003-1.063 1.86-2.03 2.173c-1 .324-3.266.633-3.815 2.17m-.075 4.343c-.244.683-1.02 1.032-1.736.779h-.001c-.716-.254-1.098-1.014-.854-1.697v-.001c.245-.684 1.022-1.032 1.737-.779q0 0 0 0c.716.254 1.098 1.014.854 1.698M16.743 7.508c-.036.77.33 1.97.94 2.534c.54.5-.141 1.798.528 2.554c.74.838.636 1.324-.025 2.47c-1.07 1.855-1.604 3.642-1.023 6.076m5.234 4.78c-1.273.264-2.16-1.168-2.971-2.17c-1.236-1.53-2.05-2.687-3.62-2.992c-3.234-.629-4.457-5.489-2.113-7.129c.816-.57 2.056-.764 2.152-2.177c.065-.966-.603-.702-1.025-.612l-1.634.347c-1.164.247-.44-1.395.402-1.567m7.52 20.222c-.421-1.878-1.825-2.864-3.662-3.053c-1.07-.11-1.794-1.243-2.617-1.903c-1.01-.81-2.03-1.162-2.778-.17c-.174-.91-.856-1.386-1.4-1.917c-.576-.562-.833-1.597-1.11-2.447m3.217 9.943c1.724.092 2.114-.33 3.08-.645c.839-.274 1.785-.046 2.244.388m3.222 4.889l-2.722-1.218c-1.95-.871-1.11-3.22-.017-4.051m2.5 13.702c1.618-.279 3.303-1.907 2.624-3.436c-.325-.733-.628-1.303-.438-2.26c.34-1.714-.428-2.471-.332-4.01c.073-1.17.484-2.907.484-5.814V21.62c-1.87-1.444-.566-5.258-.463-8.074c.094-2.542.503-5.052-.19-7.91c-1.065-1.69-4.033-1.408-5.24.287c-.318.448-.913-.096-1.592-.208c-3.532-.584-4.558 3.283-5.498 6.441c-.302 1.014-.94 1.233-1.656 2.782c-.243.527.11 2.567-.882 3.401c-.87.732-1.967 1.861-1.55 3.34c.362 1.281-.928 3.15-.945 5.497c-.011 1.57 1.04 1.797 1.555 2.563c.466.694-.95 4.266 1.517 4.647c2.205.34 1.202 1.115 1.91 1.374c.516.187 1.536.456 1.997.793c1.288.941.674 2.868 2.1 3.793l4.569 2.966c.494.32 1.409.157 2.03.05m19.424-18.705c.658-1.188 1.915-2.32 1.737-3.857c-.143-1.228-1.46-1.649-2.335-3.019c-.508-.793-.018-2.33-1.751-4.11c-1.152-1.18-1.158-2.862-1.675-4.15c-.697-1.74-2.09-3.717-3.574-3.687c-.977.02-1.898 1.003-2.927-.26c-1.123-1.378-3.983-.493-3.757 1.98c-1.577 1.349-2.07 3.559-1.682 5.483c.25 1.234-.475 2.38-.286 4.055c.096.843.702 1.118.534 2.483c-.184 1.49.98 1.935.678 2.966c-.332 1.134-.362 2.085-.207 2.96c.21 1.193.265 2.395-.087 3.593c-.367 1.984-1.201 3.628.085 5.98c-.7 1.806-.38 3.613.048 5.42c-.048 2.955 2.4 3.73 4.708 2.084a15.6 15.6 0 0 1 3.309-2.038c1.757-.808 1.869-1.558 2.183-2.44c.216-.751.909-1.181 1.702-1.38c.725-.183.607-.99 1.01-1.442c.485-.542 1.064-.684 1.643-.944c.975-.44 1.233-1.364 1.1-2.71c-.2-2.006.567-2.325 1.137-3.075c1.02-1.34.395-3.238-.392-5.6"/></svg>    
        <div class="flex flex-col p-4.5 bg-[url('$lib/assets/radial.png')] bg-center bg-contain bg-no-repeat">
            <div class="grid grid-cols-6 grid-rows-6 pr-6 gap-1.5 text-slate-gray text-2xl font-semibold font-tt-hoves">
                <div class="flex bg-off-white p-3 rounded-2xl row-start-1 row-span-3 col-start-2 col-span-2">
                    <img src={leaves} alt="leaves" height="150" width="150" class="self-start">
                    <span class="w-full text-right">What is it?</span>
                </div>
                <div class="flex bg-off-white p-3 rounded-2xl row-start-2 row-span-2 col-start-4 col-span-3 w-fit">
                    <span class="self-end w-full">Why do we need it?</span>
                    <img src={circle} alt="circle" height="120" width="120" class="self-start">
                </div>
                <div class="flex-col bg-off-white p-3 rounded-2xl row-start-4 row-span-2 col-start-2 col-span-2 w-fit">
                    <span>What is the scope for the future?</span>
                    <img src={star} alt="star" height="100" width="100">
                </div>
                <div class="grid grid-rows-2 bg-off-white p-3 rounded-2xl row-start-4 row-span-3 col-start-4 col-span-2 w-fit">
                    <img src={smallarch} alt="arch" height="100" width="100">
                    <span>How does ABIT contribute to the study?</span>
                </div>
            </div>
        </div>
    </div>
</div>

<div class="px-4 flex">
    <Boxset></Boxset>
    <div class="self-center" use:inView={2}>
    {#if whatwedoVisible}
        <span class="px-4.5 text-5xl text-royal-blue font-tt-hoves font-bold" transition:fly={{delay:100, y:100, duration:1000}}>What We Do?</span>
    {:else}
        <span class="px-4.5 text-5xl text-royal-blue font-tt-hoves font-bold opacity-0">What We Do?</span>
    {/if}
    </div>
</div>
<Breadcrumbs></Breadcrumbs>

<div class="flex">
    <div class="px-4 py-2 flex flex-col gap-4 flex-none">
        <Boxset></Boxset>
        <div class="bg-uninteresting-yellow mx-3 text-uninteresting-yellow flex-auto w-6"></div>
    </div>
    <div class="relative -bottom-21">
        <div use:inView={3}>
        {#if partnersVisible}
            <span class="py-2 text-5xl text-too-red font-tt-hoves font-bold" transition:fly={{delay:200, y:100, duration:1000}}>Partners</span>
        {:else}
            <span class="py-2 text-5xl text-too-red font-tt-hoves font-bold opacity-0">Partners</span>
        {/if}
        </div>
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

<div class="grid grid-cols-1 grid-rows-1 h-90 bg-[url('$lib/assets/abit.png')] bg-center bg-contain bg-no-repeat">
    <span class="backdrop-blur-md text-royal-blue text-8xl text-center font-unbounded font-extrabold self-center py-33">
        Connect
    </span>
</div>