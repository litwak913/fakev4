<script lang="ts">
    import { Row, Col, Tabs, Tab } from "svelte-chota";
    let type_list:Array<string>=new Array(
        '全部',
        '服务器插件',
        '模组',
        '软件',
        '地图',
        '资源包',
        '整合包',
        '数据包'
    );
    let img_list:Array<string>=new Array(
        '/icons/all.png',
        '/icons/plugins.png',
        '/icons/mods.png',
        '/icons/software.png',
        '/icons/map.png',
        '/icons/resourcespack.png',
        '/icons/modpack.png',
        'https://via.placeholder.com/160'
    );
    
    let class_name:string="全部"
    let img_src:string="/icons/all.png"
    let active_tab:number
    $: {
        class_name=type_list[active_tab]
        img_src=img_list[active_tab]
    }
</script>

<Row>
    <Col size="8">
        <Row>
            <Col size="3"><img src={img_src} width="160" height="160"/></Col>
            <Col size="9">
                <h1>{class_name}</h1>
                <p class="text-grey">{class_name}</p>
            </Col>
        </Row>
        <div>
            <Tabs bind:active={active_tab}>
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
