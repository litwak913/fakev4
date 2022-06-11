<script lang="ts">
	import "chota";
	import { Container, Row, Col } from "svelte-chota";
	import {faker} from "@faker-js/faker"
	import AppBar from "./AppBar.svelte";
	import ResCard from "./components/ResCard.svelte";
	import Banner from "./Banner.svelte";
	import Aside from "./components/HomeAside.svelte";
</script>

<AppBar />
<Container style="padding-top:20px;">
	<Banner />
	<Row>
		<Col size="9">
			<div class="grid">
				{#each [1,2,3,4,5,6,7,8] as i}
					<ResCard user={faker.internet.userName()} unixtimestamp={faker.date.recent().valueOf()}/>
				{/each}
			</div>
		</Col>
		<Col size="3">
			<Aside/>
		</Col>
	</Row>
</Container>
<style>
	:global(:root) {
		--grid-maxWidth: 120rem !important;
		--color-primary: #4caf50 !important;
	}
	.grid {
		display: grid;
		grid-template-columns: repeat(2,calc(75% - var(--grid-gutter)));
                width: calc(75% - var(--grid-gutter));
		/* grid-column-gap: 20px; */
	}
</style>
