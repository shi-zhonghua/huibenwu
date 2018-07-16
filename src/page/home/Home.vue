<template>
	<div>
		<pulic-header></pulic-header>
		<div class="main">
			<home-slide></home-slide>
			<home-hotrecom></home-hotrecom>
			<home-lovesread></home-lovesread>
		</div>
		<pulic-footer></pulic-footer>
	</div>
</template>

<script>

import PulicHeader from '../header/Header'
import PulicFooter from '../header/Footer'
import HomeSlide from './components/Slide'
import HomeHotrecom from './components/Hotrecom'
import HomeLovesread from './components/Lovesread.vue'
export default {
	name: 'Home',
	components: {
  		PulicHeader,
  		PulicFooter,
  		HomeSlide,
  		HomeHotrecom,
  		HomeLovesread
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