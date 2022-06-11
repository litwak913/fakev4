<script lang="ts">
    import { Card, Tag, Icon, Row, Col } from "svelte-chota";
    import moment from 'moment';
    import { mdiAccount, mdiClockOutline } from "@mdi/js";
    export let tags:Array<string>=["1.16.5","test"];
    export let title:string="Test"
    export let des:string="test test"
    export let user:string="User"
    export let unixtimestamp:number=1654947858884
    export let imgsrc:string="https://via.placeholder.com/80"
</script>

<div class="res">
<Card>
    <Row>
        <Col size="4"><img src="{imgsrc}" alt="{title}"/></Col>
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
    <span class="text-grey">{moment(unixtimestamp).format("YYYY/MM/DD HH:mm:ss")}</span>
</Card>
</div>

<style>
    .res-title {
        font-size: 150%;
    }
    .res {
        width: calc(100% - var(--grid-gutter));
        margin: 10px 0;
        page-break-inside: avoid;
    }
</style>
