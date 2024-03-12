<script>
    import "../app.css";
    import Logo from "$lib/images/logo.svelte";
    import CTA from "$lib/components/cta_btn.svelte";
    import Pfp from "$lib/images/pfp.png";

    let name = "John Doe";
</script>

<div class="w-full h-full px-10 pt-4 flex flex-col justify-between bg-[#fcfcff]">
    <div class="flex items-center justify-between border-b border-gray-400 border-dotted pb-4">
        <Logo width="100" />
        <div class="flex items-center justify-between">
            <div class="flex items-center justify-between text-gray-500 text-sm mr-6">
                <a href="/" class="mr-7">
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 2 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-home inline-flex items-center mr-1"><path d="m3 9 9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/>
                    </svg>
                    Home
                </a>
                <a href="/" class="mr-7">
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-telescope inline-flex items-center mr-1"><path d="m10.065 12.493-6.18 1.318a.934.934 0 0 1-1.108-.702l-.537-2.15a1.07 1.07 0 0 1 .691-1.265l13.504-4.44"/><path d="m13.56 11.747 4.332-.924"/><path d="m16 21-3.105-6.21"/><path d="M16.485 5.94a2 2 0 0 1 1.455-2.425l1.09-.272a1 1 0 0 1 1.212.727l1.515 6.06a1 1 0 0 1-.727 1.213l-1.09.272a2 2 0 0 1-2.425-1.455z"/><path d="m6.158 8.633 1.114 4.456"/><path d="m8 21 3.105-6.21"/><circle cx="12" cy="13" r="2"/></svg>
                    Explore
                </a>
                <a href="/" >
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-graduation-cap inline-flex items-center mr-1"><path d="M21.42 10.922a1 1 0 0 0-.019-1.838L12.83 5.18a2 2 0 0 0-1.66 0L2.6 9.08a1 1 0 0 0 0 1.832l8.57 3.908a2 2 0 0 0 1.66 0z"/><path d="M22 10v6"/><path d="M6 12.5V16a6 3 0 0 0 12 0v-3.5"/></svg>
                    Learn
                </a>
            </div>
            <!-- Post CTA Button -->
            <CTA class="text-gray-700 px-4 py-1 rounded-[0.29rem] text-sm font-medium bg-white border border-gray-700 flex items-center hover:bg-[#0066ff] hover:text-white drop-shadow-[0_3px_0_rgb(55,65,81,1)] hover:drop-shadow-[0_3px_0_rgb(0,58,145)] hover:border-[#0066ff] transition-all duration-200 cursor-pointer" text="Post" iconType="plus"/>

            <!-- User controls -->
            <div class="flex items-center justify-between ml-7 rounded-lg m-0 hover:bg-slate-100 p-1 px-2 cursor-pointer">
                <img src={Pfp} alt="Krishna Kiran" class="w-7 h-7 rounded-full mr-3 border border-gray-400" />
                <div class="text-sm font-medium tracking-tight text-gray-700">Krishna Kiran</div>
                <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-chevron-down ml-2"><path d="m6 9 6 6 6-6"/></svg>
            </div>
        </div>
    </div>

    <!-- Content -->
    <div class="px-[10rem] mt-10 min-h-max">
        <slot />
    </div>
    <div class="h-px w-full border-b border-dashed border-gray-400 mb-10"></div>
</div>