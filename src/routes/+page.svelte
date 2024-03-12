<script>
    import Userbio from "$lib/components/user-bio.svelte";
    import CTA from "$lib/components/cta_btn.svelte";
	import TimelineItem from "../lib/components/timeline-item.svelte";
</script>

<div class="w-auto min-h-max px-[5rem]">
    <Userbio />

    <div class="mt-10 h-full ml-16">
        <!-- Timeline -->
        <TimelineItem itemDate="Dec 2023" itemType="post" card1="No amount of technology can convert a bad story into a good story." card2="Most people don't have original ideas. Here is how Sam Altman pushes himself to have unpopular ideas." photo1="Photo 4" photo2="Photo 3"/>
        <TimelineItem itemDate="Joined - Nov 2023" jobType="Full-time" location="San Francisco Bay Area" itemType="job" jobLocation="Remote"/>
        <TimelineItem itemDate="Dec 2023" itemType="post" card1="Startup Lesson I am reflecting. Don't build for &quot;average person&quot;." card2="Your biggest regrets at 80 will be acts of omission." />
        <TimelineItem itemDate="Joined - Sep 2022" jobType="Full-time" location="San Francisco Bay Area" itemType="job" companyName="BetterUp" companyRole="VP Engineering" companyLogo="https://media.licdn.com/dms/image/C4D0BAQFLI3Q4odBnlA/company-logo_200_200/0/1654006359450/betterup_logo?e=2147483647&v=beta&t=ApbBeFWfyv9z8IeYOapiOUW8ckswN_Zx5QwJ-HOjyW0"/>
    </div>
</div>
