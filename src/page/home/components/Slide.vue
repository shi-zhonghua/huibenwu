<template>
	<div class="slide-show" @mouseover="clearInv" @mouseout="runInv">
		<div class="slide-img">
			<img :src="list[nowIndex].imgUrl" />
		</div>
		<h2>{{list[nowIndex].title}}</h2>
		<ul class="slide-pages" >
			 <li @click="gotos(prevIndex)">&lt;</li>
			<li 
				v-for="(item,index) in list"
				@click="gotos(index)"
				:class="{on: index === nowIndex}"
			>
				{{index+1}}
			</li>
			<li @click="gotos(nextIndex)">&gt;</li>
		</ul>
	</div>
</template>

<script >
	export default {
		name: 'Slide',
		methods: {
			gotos (index) {
				this.nowIndex = index
			},
			runInv () {
		      this.invId = setInterval(() => {
		        this.gotos(this.nextIndex)
		      }, 3000)
		    },
		    clearInv () {
		      clearInterval(this.invId)
		    }
		},
		computed: {
			prevIndex () {
				if(this.nowIndex===0){
					return this.list.length - 1
				}else {
					return this.nowIndex -1
				}
			},
			nextIndex () {
		      if (this.nowIndex === this.list.length - 1) {
		        return 0
		      }
		      else {
		        return this.nowIndex + 1
		      }
		    }
		},
		mounted () {
			this.runInv();
		},
		data () {
			return {
				nowIndex:0,
				list:[{
					id:'001',
					imgUrl:require('../../../assets/images/banner_01.jpg'),
					title: '1'
				},{
					id:'002',
					imgUrl:require('../../../assets/images/banner_02.jpg'),
					title: '2'
				},{
					id:'003',
					imgUrl:require('../../../assets/images/banner_03.jpg'),
					title: '3'
				}]
			}
		}
	}
</script>

<style lang="less" scoped>
.slide-show {
  position: relative;
  width: 100%;
  height: 220px;
  overflow: hidden;
  background:#ff0;
  margin-top:20px;
}
.slide-show h2 {
  position: absolute;
  width: 100%;
  height: 100%;
  color: #fff;
  background: #000;
  opacity: .5;
  bottom: 0;
  height: 30px;
  line-height:30px;
  text-align: left;
  padding-left: 15px;
  margin:0;
  font-size:12px;
}
.slide-img {
  width: 100%;
}
.slide-img img {
  width: 100%;
  height:100%;
  position: absolute;
  top: 0;
}
.slide-pages {
  position: absolute;
  bottom: 6px;
  right: 15px;
  margin:0;
}
.slide-pages li {
  display: inline-block;
  padding: 2px 10px;
  cursor: pointer;
  color: #fff;
}
.slide-pages li.on {
  //text-decoration: underline;
  background:#ff9228;
  color:#fff;
  border-radius: 8px;
}
</style>