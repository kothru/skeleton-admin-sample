<script>
	import { Accordion, AccordionItem, AppBar } from '@skeletonlabs/skeleton';
	import Icon from '@iconify/svelte';
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
