<template>
		<div>
			<div class="title">周末去哪儿</div>
			<ul>
				<li class="item border-bottom"  v-for='item of RecommendList' :key="item.id">
					<div class="item-img-wrapper">
						<img class="item-img" :src="item.imgUrl">
					</div>
					<div class="item-info">
						<p class="item-title">{{item.title}}</p>
						<p class="item-desc">{{item.desc}}</p>
					</div>
				</li>
			</ul>
		</div>
</template>

<script>
export default{
	name:'HomeWeekend',
	data (){
		return {
			RecommendList:[
			{
				id:'0001',
				imgUrl:'http://img1.qunarzz.com/sight/source/1505/4e/3e87ee62e59cdb.jpg_r_640x214_fe6cc902.jpg',
				title:'宋城千古情',
				desc:'创造世界演艺史传奇'
			},
			{
				id:'0002',
				imgUrl:'http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg',
				title:'最忆是杭州',
				desc:'G20峰会特别版《印象西湖》'
			},
			{
				id:'0003',
				imgUrl:'http://img1.qunarzz.com/sight/source/1505/bc/83feb2e003d0dd.jpg_r_640x214_0b7269b8.jpg',
				title:'千岛湖森林氧吧',
				desc:'浙江省最佳生态景点'
			},
			{
				id:'0004',
				imgUrl:'http://img1.qunarzz.com/sight/source/1505/ae/4fe23c6b6679e2.jpg_r_640x214_368a18d8.jpg',
				title:'杭州海底世界',
				desc:'集休闲、观光、科普为一体的现代化海洋生物博览馆'
			},
			{
				id:'0005',
				imgUrl:'http://img1.qunarzz.com/sight/source/1505/c1/1178c5696fcf57.jpg_r_640x214_a69542c6.jpg',
				title:'双溪竹海漂流',
				desc:'创造世界演艺史传奇'
			},
			
		]
		}
	}
}

</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
	.title
		line-height:.6rem
		background #eee
		text-indent:.2rem
		margin-top:.2rem
	.item-img-wrapper
		overflow:hidden
		height:0
		padding-bottom:33.9%
	.item-img
		width:100%
	.item-info
		padding:.1rem
		.item-title
			line-height:.54rem
			font-size:.32rem
			ellipsis()
		.item-desc
			line-height:.4rem
			color:#ccc
			ellipsis()

</style>