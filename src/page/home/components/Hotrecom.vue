<template>
	<div class="hotrecom">
		<h2>热门推荐</h2>
		<ul class="list">
			<li v-for="(item,index) in list" :key="index">
				<div class="list-img"><img :src="item.imgUrl"/></div>
				<div class="list-info">
					<div class="info-name">{{item.name}}</div>
					<div class="info-name">{{item.title}}</div>
				</div>
				<div class="bottom" @click="handleJieyueClick(index)">借阅</div>
			</li>
		</ul>
	</div>
</template>

<script>

export default {
	name: 'Hotrecom',
	methods: {
		handleJieyueClick (index) {
			console.log(this.list[index].name);
		}
	},
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
	.hotrecom{
		margin-top:10px;
		width:49%;
		float:left;
	    overflow: hidden;
	}
	.hotrecom h2{
		line-height:28px;
		border-bottom:solid 2px #ff9228;
		font-size:16px;
		color:red;
		font-weight:bold;
	}
	.list li{
		float:left;
		width:31%;
	    overflow: hidden;
	    margin:5px;
	    box-sizing:border-box;
	    padding:3px;
	}
	.list-img{
		width:100%;
		height:150px;
		overflow:hidden;
	}
	.list-img img{
		display:block;
		width:100%;
		height:100%;
		overflow:hidden;
	}
	.list-info{
		margin-top:5px;
	}
	.info-name{
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