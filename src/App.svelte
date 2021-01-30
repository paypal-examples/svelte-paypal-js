<script>
	import Item from './Item.svelte';
	import Checkout from './Checkout.svelte';
</script>

<main>
  <h1>Buy a plant!</h1>
	<Item />
	<Checkout />
</main>

<style>
	main {
		font-family: "Roboto", sans-serif;
		width: 350px;
		margin: auto;
		padding: 20px;
		position: relative;
		background: #ffffff;
		text-align: center;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	h1 {
		font-size: 65px;
		font-weight: bold;
	}
</style>