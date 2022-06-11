<script lang="ts">
	//import {faker} from "@faker-js/faker"
	import { Row, Col,Field,Button } from "svelte-chota";
	import ResCard from "../components/ResCard.svelte";
	import Banner from "../Banner.svelte";
	import Aside from "../components/HomeAside.svelte";
	import {mdiViewAgendaOutline,mdiViewHeadline} from "@mdi/js"
</script>
<Banner />
<Row>
	<Col size="9">
	<Row>
	<Col size="10">
		<Field gapless>
			<Button primary>10</Button>
			<Button outline>20</Button>
			<Button outline>50</Button>
			<Button outline>100</Button>
		</Field>
	</Col>
	<Col size="2" class="is-horizontal-align">
		<Field gapless>
			<Button primary icon={mdiViewAgendaOutline} />
			<Button outline icon={mdiViewHeadline} />
		</Field>
	</Col>
	</Row>
	<div class="grid">
		{#each [1,2,3,4,5,6,7,8] as i}
			<ResCard />
		{/each}
	</div>
	</Col>
	<Col size="3">
		<Aside/>
	</Col>
</Row>
<style>
	.grid {
		display: grid;
		grid-template-columns: repeat(2,calc(75% - var(--grid-gutter)));
                width: calc(75% - var(--grid-gutter));
	}
	:global(.message) {
		display:none;
	}
</style>
