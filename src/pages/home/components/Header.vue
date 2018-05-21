<template>
		<div class="header">
	 			<div class="header-left"><div class="iconfont">&#xe624;</div></div>
				<div class="header-input"><span class="iconfont">&#xe632;</span>输入城市/景点/游玩主题</div>
				<router-link to='/city'>
					<div class="header-right">{{this.$store.state.city}}<span class="iconfont arrow-icon">&#xe64a;</span></div>
				</router-link>
		</div>
</template>

<script>
export default {
	name: 'HomeHeader',
}
</script>

<style lang="stylus" scoped>
	@import '~styles/varibles.styl'
	.header
		display:flex
		line-height:$headerHeight
		background:$bgColor
		xalign-items:center
		color:#fff
		.header-left
			width:.64rem
			float:left
			text-align:center
		.header-input
			flex:1
			height:.64rem
			line-height:.64rem
			text-align:center
			border-radius:.1rem 
			margin:.12rem .2rem
			background:#fff
			color:#ccc
		.header-right
			width:1.24rem
			float:right
			text-align:center
			color:#fff
			.arrow-icon
				font-size 0.24rem
			
</style>