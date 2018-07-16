<template>
	<div>
		<pulic-header></pulic-header>
		<div class="main">
			<list-show></list-show>
			<public-fenye></public-fenye>
		</div>
		<pulic-footer></pulic-footer>
	</div>
	
</template>

<script>
import PulicHeader from '../header/Header'
import PulicFooter from '../header/Footer'
import ListShow from './components/listshow'
import PublicFenye from './components/fenye'
export default {
	name: 'HuibenShow',
	components: {
		PulicHeader,
		PulicFooter,
		ListShow,
		PublicFenye
	}
}
</script>

<style lang="less" scoped>
	.main{
		width:900px;
		margin:0 auto;
		overflow:hidden;
		padding-bottom:60px;
	}
</style>