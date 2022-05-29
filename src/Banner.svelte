<script lang="ts">
    import { Row, Col, Tabs, Tab } from "svelte-chota";
</script>

<Row>
    <Col size="8">
        <Row>
            <Col size="3"><img src="https://via.placeholder.com/160" /></Col>
            <Col size="9">
                <h1>全部</h1>
                <p class="text-grey">全部资源</p>
            </Col>
        </Row>
        <div>
            <Tabs>
                <Tab>全部</Tab>
                <Tab>服务器插件</Tab>
                <Tab>模组</Tab>
                <Tab>软件</Tab>
                <Tab>地图</Tab>
                <Tab>资源包</Tab>
                <Tab>整合包</Tab>
                <Tab>数据包</Tab>
            </Tabs>
        </div>
        
    </Col>
    <Col size="4"><img src="https://via.placeholder.com/408x180" /></Col>
</Row>
