<script lang="ts">
	import {Nav} from 'svelte-chota'
	export let name: string;
</script>

<header>
	<Nav class="nav">

	</Nav>
</header>

<style>
	header {
		background-color: #4caf50;
		width: 100%;
		height: 10%;
		padding:0;
		box-shadow: 2px 0px 4px #000000;
	}
	.nav {
		width: 60%;
		margin: 0 0 auto;
	}
</style>