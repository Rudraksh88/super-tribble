<script>
    import photo1 from '$lib/images/photo1.png';
    import photo2 from '$lib/images/photo2.png';
    import photo3 from '$lib/images/sam.png';
    import photo4 from '$lib/images/steve.png';

    let photos = [
        {
            src: photo1,
            name: 'Photo 1'

        },
        {
            src: photo2,
            name: 'Photo 2'
        },
        {
            src: photo3,
            name: 'Photo 3'
        },
        {
            src: photo4,
            name: 'Photo 4'
        }
    ]

    export let photoName = 'Photo 1';
    export let cardContent = 'Some card desc';

    let photoToDisplay = photos.find(photo => photo.name === photoName).src;
    // console.log(photoToDisplay)
</script>

<div class="rounded-lg flex flex-col h-full w-80 border border-gray-200 overflow-hidden shadow-sm mr-4">
    <img src="{photoToDisplay}" alt="" class="object-cover max-h-[150px]">
    <div class="bg-white p-4 h-[72px] text-sm tracking-tight flex-shrink-0">
        <div class="line-clamp-2">{cardContent}</div>
    </div>
</div>
