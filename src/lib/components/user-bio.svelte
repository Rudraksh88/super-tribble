<script>
    import CTA from './cta_btn.svelte';
    import Pfp from '$lib/images/pfp.png'

    export let name = 'Krishna Kiran';
    export let bio = `Co-Founder and CEO at Duggup - Social network for people in tech. Ex-Amazon Head
Of Engineering. I write hot-takes on building a business, shipping delightful products and
accelerating product and career growth.`;
    export let avatar = Pfp;
    export let company = 'Duggup';
    export let companyRole = 'Co-Founder and CEO';
    export let companyLogo = 'https://is1-ssl.mzstatic.com/image/thumb/Purple126/v4/11/5a/f0/115af004-378e-cf28-95b2-21de2afd5853/AppIcon-0-0-1x_U007emarketing-0-10-0-85-220.png/512x512bb.jpg';
    export let followed = false;
</script>

<div class="flex items-center justify-between">
    <div class="flex items-start">
        <img src={avatar} alt={name} class="w-32 rounded-full mr-6 border-4 border-gray-200" />
        <div class="ml-4">
            <h1 class="text-3xl font-bold tracking-tight mb-2 text-gray-700">{name}</h1>
            <p class="text-gray-500 text-sm mb-4">{bio}</p>
            <CTA class="text-gray-700 px-4 py-1 w-max rounded-[0.29rem] text-sm font-medium bg-white border border-gray-700 flex items-center hover:bg-[#0066ff] hover:text-white drop-shadow-[0_3px_0_rgb(55,65,81,1)] hover:drop-shadow-[0_3px_0_rgb(0,58,145)] hover:border-[#0066ff] transition-all duration-200 cursor-pointer" text={ followed ? 'Followed' : 'Follow' } />
        </div>

        <!-- Company details -->
        <!-- Company logo in a circle -->
        <div class="ml-16 flex flex-col items-end">
            <img src={companyLogo} alt="duggup-logo" class="rounded-full w-10 mb-1">
            <div class="min-w-max text-right mb-7">
                <div class="text-md font-bold tracking-tight mb-1">{company}</div>
                <div class="text-xs text-gray-500 tracking-tight">{companyRole}</div>
            </div>
            <div class="text-xs text-gray-700 tracking-tight font-medium cursor-pointer flex items-center justify-between w-max">
                <div class="px-2 p-1 hover:bg-slate-100 rounded h-6 flex items-center">My Website ↗</div>
                <div class="ml-2 hover:bg-slate-100 px-1 rounded flex items-center h-6">
                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-ellipsis"><circle cx="12" cy="12" r="1"/><circle cx="19" cy="12" r="1"/><circle cx="5" cy="12" r="1"/></svg>
                </div>
            </div>
        </div>
    </div>
</div>