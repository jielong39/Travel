<template>
		<div>
			<div class="title">热销推荐</div>
			<ul>
				<li class="item border-bottom"  v-for='item of RecommendList' :key="item.id">
					<img class="item-img" :src="item.imgUrl">
					<div class="item-info">
						<p class="item-title">{{item.title}}</p>
						<p class="item-desc">{{item.desc}}</p>
						<button class="item-button">查看详情</button>
					</div>
				</li>
			</ul>
		</div>
</template>

<script>
export default{
	name:'HomeRecommend',
	data (){
		return {
			RecommendList:[
			{
				id:'0001',
				imgUrl:'http://img1.qunarzz.com/sight/p0/1412/be/c788f0f3767d2ea037b9b66d2010bfa4.water.jpg_200x200_ead93bcd.jpg',
				title:'宋城千古情',
				desc:'创造世界演艺史传奇'
			},
			{
				id:'0002',
				imgUrl:'http://img1.qunarzz.com/sight/p0/1709/28/288fbeccc335f774a3.img.jpg_200x200_4a81bde9.jpg',
				title:'最忆是杭州',
				desc:'G20峰会特别版《印象西湖》'
			},
			{
				id:'0003',
				imgUrl:'http://img1.qunarzz.com/sight/p0/201406/24/e2a5766e6e81793b2b518a7a08812a4a.jpg_200x200_66ce1370.jpg',
				title:'千岛湖森林氧吧',
				desc:'浙江省最佳生态景点'
			},
			{
				id:'0004',
				imgUrl:'http://img1.qunarzz.com/sight/p0/201212/18/f195032e85740a4b93835fbb.jpg_200x200_77761d11.jpg',
				title:'杭州海底世界',
				desc:'集休闲、观光、科普为一体的现代化海洋生物博览馆'
			},
			{
				id:'0005',
				imgUrl:'http://img1.qunarzz.com/sight/p0/1603/e6/e646f4221574cc2a90.water.jpg_200x200_d9b6cabd.jpg',
				title:'双溪竹海漂流',
				desc:'创造世界演艺史传奇'
			},
			{
				id:'0006',
				imgUrl:'http://img1.qunarzz.com/sight/p0/1603/38/38530bbf8ed47e490.water.jpg_200x200_b1556ec5.jpg',
				title:'钱塘江夜游',
				desc:'G20峰会特别版《印象西湖》'
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
	.item
		overflow:hidden
		display:flex
		height:1.9rem
		.item-img
			width:1.7rem
			height:1.7rem
			padding:.1rem
		.item-info
			flex:1
			padding:.1rem
			min-width:0
			.item-title
				line-height:.54rem
				font-size:.32rem
				ellipsis()
			.item-desc
				line-height:.4rem
				color:#ccc
				ellipsis()
			.item-button
				line-height:.44rem
				margin-top:.2rem
				background:#ff9300
				padding:0 .2rem
				border-radius:.06rem
				color:#fff
</style>