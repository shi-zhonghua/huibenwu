<template>
	<div class="listshow">
		<ul>
			<li class="listshow-li" v-for="(item,index) in list">
				<img class="listshow-img" :src="item.imgUrl">
				<div class="list-show-name">{{item.name}}</div>
				<div class="list-show-name">{{item.title}}</div>
				<div class="bottom">借阅</div>
			</li>
			
		</ul>
	</div>
</template>

<script>

export default {
	name: 'ListShow',
	data () {
		return {
			list:[{
				id:'0001',
				name: '谁藏起来了谁藏起来了谁藏起来了谁藏起来了',
				imgUrl:require('../../../assets/images/2018101755.jpg'),
				title: '亲子阅读 0-12岁',
			},{
				id:'0002',
				name: '谁藏起来了',
				imgUrl:require('../../../assets/images/2018101755.jpg'),
				title: '亲子阅读 0-12岁'

			},{
				id:'0003',
				name: '谁藏起来了',
				imgUrl:require('../../../assets/images/2018101755.jpg'),
				title: '亲子阅读 0-12岁'
			},{
				id:'0004',
				name: '谁藏起来了',
				imgUrl:require('../../../assets/images/2018101755.jpg'),
				title: '亲子阅读 0-12岁'
			},{
				id:'0005',
				name: '谁藏起来了',
				imgUrl:require('../../../assets/images/2018101755.jpg'),
				title: '亲子阅读 0-12岁'
			},{
				id:'0006',
				name: '谁藏起来了',
				imgUrl:require('../../../assets/images/2018101755.jpg'),
				title: '亲子阅读 0-12岁'
			}]
		}
	}
}
</script>

<style lang="less" scoped>

	.listshow ul{
		margin-top:20px;
		box-sizing:border-box;
		width:100%;
		padding: 8px;
		overflow:hidden;
	}
	.listshow-li{
		padding:10px;
		float:left;
		width:25%;
		box-sizing:border-box;
		
	}
	.listshow-li:hover{
		box-shadow:0px 0px 2px #ccc;
		
	}
	.listshow-img{
		width:100%;
		height:150px;
		overflow:hidden;
	}
	.listshow-img img{
		width:100%;
		height:100%;
		overflow:hidden;
	}
	.list-show-name{
		color:#666;
		padding:6px 0;
		font-size:12px;
		overflow: hidden;
	    white-space: nowrap;
	    text-overflow: ellipsis;
	}
	.bottom{
		float:right;
		background: #df3033;
		color: #fff;
		padding: 5px 20px;
		margin-top:10px;
		cursor: pointer;
	}
	


</style>