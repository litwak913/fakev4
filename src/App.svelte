<script lang="ts">
	import "chota";
	import { Container } from "svelte-chota";
	import AppBar from "./AppBar.svelte";
	import Router from 'svelte-spa-router';
	import routes from "./routes.ts"
</script>

<AppBar />
<Container style="padding-top:20px;">
	<Router {routes} />
</Container>
<style>
	:global(:root) {
		--grid-maxWidth: 120rem !important;
		--color-primary: #4caf50 !important;
	}
</style>
