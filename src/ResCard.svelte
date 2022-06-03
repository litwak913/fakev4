<script lang="ts">
    import { Card, Tag, Icon, Row, Col } from "svelte-chota";
    import { mdiAccount, mdiClockOutline } from "@mdi/js";
    export let tags:Array<string>=["1.16.5","test"];
    export let title:string="Test"
    export let des:string="Lorem ipsum dolor sit amet, consectetur adipiscing elit sed do eiusmod tempor incididunt ut labore"
    export let user:string="User"
    export let time:number=0
</script>

<div class="res">
<Card>
    <Row>
        <Col size="4"><img src="https://via.placeholder.com/80" /></Col>
        <Col size="8">
            <div>
                <p class="is-marginless res-title">{title}</p>
                <p>{des}</p>
            </div>
        </Col>
    </Row>
    <div style="margin-bottom: 10px;">
        {#each tags as tag}
        <Tag small>{tag}</Tag>
        {/each}
    </div>
    <hr class="is-marginless" />
    <Icon class="text-grey" src={mdiAccount} />
    <span class="text-grey">{user}</span>
    <Icon class="text-grey" src={mdiClockOutline} />
    <span class="text-grey">1970/01/01 08:00:00</span>
</Card>
</div>

<style>
    .res-title {
        font-size: 150%;
    }
    .res {
        width: 430px;
        margin: 10px 0;
        page-break-inside: avoid;
    }
</style>
