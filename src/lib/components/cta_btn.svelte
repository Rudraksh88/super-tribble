<script>
    export let text = 'Button';
    export let iconType = '';

    let icons = [
        {
            name: 'home',
            svg: '<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 2 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-home inline-flex items-center mr-1"><path d="m3 9 9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/></svg>'
        },
        {
            name: 'plus',
            svg: `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-square-plus inline-flex mr-1.5"><rect width="18" height="18" x="3" y="3" rx="2"/><path d="M8 12h8"/><path d="M12 8v8"/></svg>`
        }
    ]

    let icon = icons.find(i => i.name === iconType)?.svg || '';
</script>

<div class={$$props.class}>
    <div class="mb-1">
        {@html icon}
    </div>
    <div class="mb-0.5">
        { text }
    </div>
</div>