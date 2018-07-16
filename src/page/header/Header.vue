<template>
	<div class="header">
		<div class="header-main">
			<div class="logo">
				<img src="../../assets/images/hbw_logo.png" height="43" width="139" />
			</div>
			<ul class="nav">
				
				<router-link
			        tag="li"
			        :class="path == item.path ? 'active' : ''"
			        v-for="(item,index) in list"
			        :to="item.path"
			        :key="index"

			      >
			        {{item.title}}
			     </router-link>
				
			</ul>
			<ul class="nav nav-right">
				<li @click="handleDengluClick">登录</li>
				<li @click="handleZhuceClick">注册</li>
			</ul>
		</div>
		<public-denglu v-show="showDenglu" @close="handleDengluCloseClick"></public-denglu>
		<public-zhuce v-show="showZhuce" @close="handleZhuceCloseClick"></public-zhuce>
	</div>
</template>

<script> 
import PublicDenglu from './components/denglu'
import PublicZhuce from './components/zhuce'
export default {
	name: 'PulicHeader',
	data () {
		return {
			showDenglu: false,
			showZhuce: false,
			path:'/home',
			list: [{
				title: '首页',
				path: '/home'
			},{
				title: '绘本展示',
				path: '/huibenshow'
			},{
				title: '阅读组合',
				path: '/h'
			},{
				title: '关于我们',
				path: '/h'
			},{
				title: '亲子阅读',
				path: '/h'
			},{
				title: '暑期活动',
				path: '/h'
			}]
		}
	},
	methods: {
		handleDengluClick () {
			this.showDenglu = true
		},
		handleZhuceClick () {
			this.showZhuce = true
		},
		handleDengluCloseClick () {
			this.showDenglu = false
		},
		handleZhuceCloseClick () {
			this.showZhuce = false
		}
	},
	components: {
		PublicDenglu,
		PublicZhuce

	},
	mounted () {
    	this.path= this.$route.path;
    }
	

}
</script>

<style lang="less" scoped>
.header{
	width: 100%;
	height: 43px;
	padding: 10px 0;
	background: #EAEDF1;
	overflow: hidden;
	border-bottom:solid 1px #ccc;
	box-shadow:2px 2px 5px #ccc
}
.header-main{
	width:900px;
	overflow:hidden;
	margin:0 auto;
}
.logo{
	float: left;
	width: 139px;
	height: 43px;
}
.nav{
	float:left;
	margin-left:30px;
}
.nav li{
	float:left;
	line-height:43px;
	padding:0 10px;
	cursor: pointer;
	font-size:12px;
	color:#666;
}
.nav li:hover{
	color:#ff9228;
}
.nav li.active{
	background:#ff9228;
	color:#fff;
	border-radius: 8px;
}
.nav-right{
	float:right;
}
</style>