<template>
	<div class="tabberWarp" >
		<div class="warp">
			<Item :key="item" :txt='item.txt' :page='item.page' @change='getVal' v-for='item in tabbarDes' :sel='selected'>
				<img :src="item.normalImg" slot='normalImg'>
				<img :src="item.activeImg" slot='activeImg'>
			</Item>
		</div>
	</div>
</template>
<script type="text/javascript">
	import Item from './Item.vue'
	export default{
		components:{
			Item
		},
		data:function(){
			return{
				selected:'skin',
				tabbarDes:[
					{
						txt:'表情',
						page:'skin',
						normalImg:require('assets/img/logo.png'),
						activeImg:require('assets/img/logo.png')
						
					},				
					{
						txt:'皮肤',
						page:'phiz',
						normalImg:require('assets/img/logo.png'),
						activeImg:require('assets/img/logo.png')
					},
					{
						txt:'词库',
						page:'thesaurus',
						normalImg:require('assets/img/logo.png'),
						activeImg:require('assets/img/logo.png')
					},
					{
						txt:'账号',
						page:'account',
						normalImg:require('assets/img/logo.png'),
						activeImg:require('assets/img/logo.png')
					},
					{
						txt:'设置',
						page:'setup',
						normalImg:require('assets/img/logo.png'),
						activeImg:require('assets/img/logo.png')
					}
				]
			}
		},
		methods:{
			getVal:function(res){
				this.selected = res;
			}
		}
	}
</script>
<style type="text/css">
	.warp{
		width: 100%;
		border-top: 1px solid #eee;
		background: #fff;
		display: flex;
		align-items: center;
		justify-content: space-around;
		font-size: 0;
	}
	.warp img{
		width: 20px;
		height: 20px;
	}
	.tabberWarp img{
		margin-top: 10px;
		margin-bottom: 5px;
 
	}
	.tabberWarp{
		position: fixed;
		bottom: 0;
		left: 0;
		width: 100%;
		padding-bottom: 5px;
		background: #fff;
	}
</style>