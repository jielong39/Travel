<template>
		<div>
				<home-header></home-header>
				<Home-swiper></Home-swiper>
				<home-icons></home-icons>
				<home-recommend></home-recommend>
				<HomeWeekend></HomeWeekend>
		</div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
export default{
	name: 'Home',
	components:{
		HomeHeader,
		HomeSwiper,
		HomeIcons,
		HomeRecommend,
		HomeWeekend
	}
}
</script>

<style>

</style>