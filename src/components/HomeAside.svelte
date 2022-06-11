<script lang="ts">
	import { mdiFileDocumentEditOutline, mdiUpload } from '@mdi/js';
	import { push } from 'svelte-spa-router'
    import {Button} from 'svelte-chota'
    const notfound = () => {
    	push('/notfound')
    }
</script>
<Button icon={mdiUpload} style="margin-bottom: 10px; justify-content: center;" primary class="is-full-width">发布资源</Button>
<br/>
<Button icon={mdiFileDocumentEditOutline} primary style="justify-content: center;" class="is-full-width" on:click={notfound}>发布教程 （404页面测试）</Button>
<hr/>
<p style="font-size:170%;">Search</p>
