<template>
	<div>
		<div class="banner" @click="handleBannerClick">
			<img class="banner-img" src="//img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_600x330_f922b488.jpg" alt="">
			<div class="banner-info">
				<div class="banner-title">故宫故宫故宫故宫故宫</div>
				<div class="banner-number"><span class="iconfont banner-icon">&#xe63b;</span>39</div>
			</div>
		</div>
		<common-gallary :imgs='imgs'
		 								v-show="showGallary"
		 								@close="handleGallaryClose"
		 								>
		</common-gallary>
	</div>
	
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
	name: 'DetailBanner',
	data () {
		return {
			showGallary: false,
			imgs: ['http://img1.qunarzz.com/sight/p0/201212/18/f195032e85740a4b93835fbb.jpg_600x330_692af2a1.jpg',
				'//img1.qunarzz.com/sight/p0/1508/a5/4003f9dd7bebf61eccbf64046e26d487.water.jpg_600x330_a80ff353.jpg']
		}
	},
	components: {
		CommonGallary
	},
	methods: {
		handleBannerClick () {
			this.showGallary = true
		},
		handleGallaryClose () {
			this.showGallary = false
		}
	}
}
</script>

<style lang="stylus" scoped>
	.banner
	 position:relative
	 overflow: hidden
		height: 0
		padding-bottom: 55%
		.banner-img
		 width:100%
		.banner-info
			display: flex
			position: absolute
			left: 0
			right: 0
			bottom: 0
			line-height:.6rem
			color: #fff
			background-image: linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,0.8))
			.banner-title
				font-size: .32rem
				flex: 1
				padding: 0 .2rem
			.banner-number
				height: .32rem
				margin-top: .14rem
				padding:0 .4rem
				line-height: .32rem
				border-radius: .2rem
				background: rgba(0,0,0,.8)
				font-size: .24rem
				.banner-icon
					font-size: .24rem
</style>