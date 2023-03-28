<script lang="ts">
	import {
		Accordion,
		AccordionItem,
		AppBar,
		Avatar,
		ConicGradient,
		FileButton,
		FileDropzone
	} from '@skeletonlabs/skeleton';
	import type { ConicStop } from '@skeletonlabs/skeleton';
	import Icon from '@iconify/svelte';
	const conicStops: ConicStop[] = [
		{ color: 'transparent', start: 0, end: 25 },
		{ color: 'rgb(var(--color-primary-500))', start: 75, end: 100 }
	];

	function onChangeHandler(e: Event): void {
		console.log('file data:', e);
	}
</script>

<AppBar>
	<svelte:fragment slot="lead">lead</svelte:fragment>
	<svelte:fragment slot="trail">trail</svelte:fragment>
	<svelte:fragment slot="headline">AppBar</svelte:fragment>
</AppBar>
<Accordion>
	<AccordionItem open>
		<svelte:fragment slot="lead"><Icon icon="material-symbols:looks-one" /></svelte:fragment>
		<svelte:fragment slot="summary">One</svelte:fragment>
		<svelte:fragment slot="content"
			>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quaerat delectus architecto eveniet
			quos molestias beatae temporibus fuga debitis hic fugit cumque ipsum ullam, vero
			necessitatibus deleniti minima cum officia accusantium!</svelte:fragment
		>
	</AccordionItem>
	<AccordionItem>
		<svelte:fragment slot="lead"><Icon icon="material-symbols:looks-two" /></svelte:fragment>
		<svelte:fragment slot="summary">Two</svelte:fragment>
		<svelte:fragment slot="content"
			>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quaerat delectus architecto eveniet
			quos molestias beatae temporibus fuga debitis hic fugit cumque ipsum ullam, vero
			necessitatibus deleniti minima cum officia accusantium!</svelte:fragment
		>
	</AccordionItem>
</Accordion>
<Avatar initials="JD" background="bg-primary-500" />
<ConicGradient stops={conicStops} spin>Loading</ConicGradient>
<FileButton name="file" on:change={onChangeHandler}>Upload</FileButton>
<FileDropzone name="dropped_file" on:change={onChangeHandler}>Upload</FileDropzone>
