<script lang="ts">
	import {Button} from "svelte-chota";
	import { push } from 'svelte-spa-router'
    const home = () => {
    	push('/')
    }
</script>
<div id="notfound">
	<div id="notfound-left">
		<span style="
    font-size: 6em;
    margin: 0 0;
    line-height: 1em;
">404</span><br><span style="
    font-size: 2em;
    /* margin: 0 0; */
">找不到页面</span><br>
	<span class="text-grey">请检查您输入的地址是否正确！</span> <br>
	<Button primary>返回上一页</Button>
	<Button on:click={home} >返回首页</Button>
	</div>
	<div id="notfound-right">
		<img src="/404.png" alt="Not Found" />
	</div>
</div>

<style>
	#notfound {
    	display: flex;
    	justify-content: center;
    	width: 700px;
    	height: 700px;
    	align-items: center;
    	margin: 0 auto;
	}
	
	img {
    	width: 400px;
    	height: 400px;
	}
</style>
