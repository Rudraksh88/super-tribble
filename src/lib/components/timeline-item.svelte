<script>
    import TCard from './timeline-card.svelte';
    import duggupLogo from '$lib/images/duggup.jpg';
    import betterupLogo from '$lib/images/betterup.jpeg';

    export let companyName = 'Duggup';
    export let companyRole = 'Co-Founder and CEO';
    export let companyLogo = companyName === 'Duggup' ? duggupLogo : betterupLogo;
    export let itemDate = 'Joined - 12th May 2021';
    export let jobType = 'Full-time';
    export let location = 'Remote';
    export let itemType = 'post';
    export let photo1 = 'Photo 1';
    export let photo2 = 'Photo 2';
    export let card1 = 'Card1 Desc';
    export let card2 = 'Card2 Desc';
    export let jobLocation;
</script>

<div class="flex items-center w-full border-l border-gray-400 border-dashed pb-10 last-of-type:pb-20">
    {#if itemType === 'post'}
        <div class="relative flex items-center">
            <div class="flex items-center justify-end absolute right-0">
                <div class="text-right mr-4 flex flex-col items-end content-end justify-end mr-[30px] w-max">
                    <div class="text-gray-500 text-sm">
                        { itemDate }
                    </div>
                </div>
                <!-- Dot -->
                <div class="absolute rounded-full w-3 h-3 bg-white border border-[3px] border-[#0066ff] -mr-[0.37rem]"></div>
            </div>
        </div>
        <div class="relative flex flex-col w-full ml-7">
            <!-- Content -->
            <div class="flex items-center">
                <TCard cardContent={ card1 } photoName={photo1}/>
                <TCard cardContent={ card2 } photoName={photo2}/>
            </div>
        </div>

    {:else if itemType === 'job'}
        <div class="relative flex items-center">
            <div class="flex items-center justify-end absolute right-0">
                <div class="text-right mr-4 flex flex-col items-end content-end justify-end mr-[30px] w-max">
                    <img src={companyLogo} alt="" class="object-cover w-10 rounded-full mb-1">
                    <div class="font-bold tracking-tight">
                        { companyName }
                    </div>
                    <div class="text-gray-500 text-xs">
                        {location}
                    </div>
                    <div class="text-gray-500 text-[10px]">
                        { itemDate }
                    </div>
                </div>
                <!-- Dot -->
                <div class="absolute rounded-full w-6 h-6 bg-white border border-[7px] border-[#0066ff] -mr-3"></div>
            </div>
        </div>
        <div class="relative flex flex-col w-full ml-7">
            <!-- Title -->
            <div class="flex flex-col p-4 pt-2 w-full bg-white rounded-lg shadow-md shadow-gray-100 tracking-tight border border-gray-200">
                <div class="font-bold text-lg">
                    {companyRole}
                </div>
                <div class="flex items-center text-gray-500 text-xs">
                    {jobType} {!jobLocation ? '' : '· ' + jobLocation}
                </div>
            </div>
        </div>
    {/if}

</div>