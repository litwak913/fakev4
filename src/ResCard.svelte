<script lang="ts">
    import { Card, Tag, Icon, Row, Col } from "svelte-chota";
    import { mdiAccount, mdiClockOutline } from "@mdi/js";
</script>

<div class="res">
<Card>
    <Row>
        <Col size="4"><img src="https://via.placeholder.com/80" /></Col>
        <Col size="8">
            <div>
                <p class="is-marginless res-title">测试标题</p>
                <p>测试描述</p>
            </div>
        </Col>
    </Row>
    <div style="margin-bottom: 10px;">
        <Tag small>1.16.5</Tag>
        <Tag small>测试</Tag>
    </div>
    <hr class="is-marginless" />
    <Icon class="text-grey" src={mdiAccount} />
    <span class="text-grey">测试用户</span>
    <Icon class="text-grey" src={mdiClockOutline} />
    <span class="text-grey">1970/01/01 08:00:00</span>
</Card>
</div>

<style>
    .res-title {
        font-size: 150%;
    }
    .res {
        width: 400px;
        margin: 10px 0;
        page-break-inside: avoid;
    }
</style>
