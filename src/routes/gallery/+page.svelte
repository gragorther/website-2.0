<script>
	import ImageGallery from '$lib/ImageGallery.svelte';
	import PageTitle from '$lib/PageTitle.svelte';

	const galleryImages = [
		{ src: 'optimized/a_bird.webp', alt: 'A bird from Valencia' },
		{
			src: 'optimized/bacteriaidkman.webp',
			alt: 'An oxygen generator using algae in tubes to generate it'
		},
		{ src: 'optimized/berry.webp', alt: "The neighbours' cat, Beri, visiting our apartment" },
		{ src: 'optimized/berry2.webp', alt: 'Beri again' },
		{ src: 'optimized/berry3.webp', alt: 'Beri sleeping' },
		{
			src: 'optimized/catusmaximus.webp',
			alt: 'A cat from a botanic garden in Spain'
		},
		{ src: 'golob.opti.webp', alt: 'A pigeon from Oslo' },
		{
			src: 'jelen.opti.webp',
			alt: 'A deer from Svalbard, photographed while searching for a trash can'
		},
		{
			src: 'pafin.opti.webp',
			alt: 'A puffin seen during a 5-hour ship journey to Pyramiden'
		},
		{ src: 'vrvi.opti.webp', alt: 'Ropes on the ship to Pyramiden' },
		{
			src: 'poti.opti.webp',
			alt: 'Signs showing distances to cities from the Svalbard airport'
		},
		{
			src: 'pyramiden.opti.webp',
			alt: 'A sign from Pyramiden. The 79˚ sign is slightly inaccurate.'
		},
		{ src: 'roze.opti.webp', alt: 'Flowers on Svalbard' },
		{ src: 'roze2.opti.webp', alt: 'More flowers from Svalbard' },
		{ src: 'roze3.opti.webp', alt: 'Even more flowers from Svalbard' },
		{
			src: 'svalbard_chicken.opti.webp',
			alt: 'The Svalbard chicken, which struggles to fly due to its chomnkness'
		},
		{
			src: 'leppogled.opti.webp',
			alt: 'A lake from the Lofoten islands, Norway'
		},
		{
			src: '/macek_rolling.jpeg',
			alt: 'A cat rolling on the floor'
		},
		{ src: '/macek_opazi.jpeg', alt: 'A cat looking at the camera surprised' },
		{ src: 'macek_on_the_floor.jpeg', alt: 'A cat on the floor' },

		{ src: 'macek_china.jpeg', alt: 'cat' }
	];
</script>

<PageTitle title="Gallery" />

<ImageGallery images={galleryImages} columns={3} />
