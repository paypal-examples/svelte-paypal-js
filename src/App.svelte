<script>
	import Item from './Item.svelte';
	import Checkout from './Checkout.svelte';
</script>

<main>
	<Item />
	<Checkout />
</main>

<style>
	main {
		text-align: center;
		max-width: 240px;
		display: flex;
		margin: 82px auto 32px;
		padding: 0 16px;
		max-width: 960px;
		flex-direction: column;
		align-items: center;
	}
</style>