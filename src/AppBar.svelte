<script lang="ts">
	import { Nav, Field, Input, Button } from "svelte-chota";
	import { mdiMagnify, mdiBell } from "@mdi/js";
</script>

<header>
	<Nav class="is-vertical-align">
		<svelte:fragment slot="left">
			<a href="/"><img src="/icon.png" /></a>
			<a href="/" class="text-white">资源</a>
			<a href="/" class="text-white">社区</a>
		</svelte:fragment>
		<svelte:fragment slot="right">
			<Field gapless class="is-vertical-align">
				<Input />
				<Button icon={mdiMagnify} />
			</Field>
			<img
				src="https://via.placeholder.com/160"
				class="is-rounded avatar"
			/>
			<Button icon={mdiBell} primary />
		</svelte:fragment>
	</Nav>
</header>

<style>
	.avatar {
		padding: 0 20px;
	}
	header {
		background-color: var(--color-primary);
		width: 100%;
		height: 60px;
		padding: 4px 100px;
		box-shadow: 2px 2px 4px rgb(0 0 0 / 30%), -2px 2px 4px rgb(0 0 0 / 30%);
		/* position: fixed; */
		box-sizing: border-box;
	}
</style>
