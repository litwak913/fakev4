<script lang="ts">
	import "chota";
	import { Container, Row, Col } from "svelte-chota";
	import AppBar from "./AppBar.svelte";
	import ResCard from "./ResCard.svelte";
	import Banner from "./Banner.svelte";
</script>

<AppBar />
<Container style="padding-top:20px;">
	<Banner />
	<Row>
		<Col size="9">
			<div class="grid">
				<ResCard />
				<ResCard />
				<ResCard />
				<ResCard />
				<ResCard />
				<ResCard />
				<ResCard />
				<ResCard />
			</div>
		</Col>
		<Col size="3" />
	</Row>
</Container>
<style>
	:global(:root) {
		--grid-maxWidth: 120rem !important;
		--color-primary: #4caf50 !important;
	}
	.grid {
		display: grid;
		grid-template-columns: 400px 400px;
		grid-column-gap: 20px;
	}
</style>
