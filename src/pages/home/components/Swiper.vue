<template>
		<div class="wrapper">
			<swiper :options="swiperOption" >
    <!-- slides -->
    		<swiper-slide v-for="item of swiperList" :key="item.id">
    			<img class="swiper-img" :src="item.imgUrl"/>
    		</swiper-slide>
    <!-- Optional controls -->
    		<div class="swiper-pagination"  slot="pagination"></div>
  		</swiper>
		</div>
</template>

<script>
	export default{
		name:'HomeSwiper',
		data (){
			return {
				swiperOption:{
					pagination: {
            el: '.swiper-pagination',
            loop:true
          },
          loop:true
          
				},
				swiperList:[
          {
          	id:'0001',
          	imgUrl:'http://img1.qunarzz.com/piao/fusion/1805/1e/30472c5c05379a02.jpg_750x200_ff29557c.jpg'
          },
          {
          	id:'0002',
          	imgUrl:'http://img1.qunarzz.com/piao/fusion/1609/f8/ef0b29100632f002.jpg_750x200_ebe20c8f.jpg',
          },
          {
          	id:'0003',
          	imgUrl:'http://img1.qunarzz.com/piao/fusion/1706/5d/a47eff229e73f302.jpg_750x200_bcc494d4.jpg',
          },
          {
          	id:'0004',
          	imgUrl:'http://img1.qunarzz.com/piao/fusion/1805/9e/f625886dec6c0402.jpg_750x200_417be630.jpg',
          },
          {
          	id:'005',
          	imgUrl:'http://img1.qunarzz.com/piao/fusion/1805/9a/c0984ec80d0f0a02.jpg_750x200_f55672ab.jpg'
          }
          ]
			}
		}
	}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
		background:#fff !important
.wrapper
	overflow:hidden
	width:100%
	height:0
	padding-bottom:26%
	background: #eee
	.swiper-img
		width:100%
	
</style>