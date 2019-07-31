<template>
	<view>
		<view class="">
			珍藏列表
		</view>
		<view class="cu-list menu-avatar">



			<view v-for="person in list" :key="person.id" class="cu-item " @tap="gotoPersonPage(person.id)">
				<view class="cu-avatar radius lg" :style="{backgroundImage:'url(' + person.src + ')', backgroundRepeat:'no-repeat', backgroundPosition:'center center', backgroundSize: 'contain'}"></view>
				<view class="content">
					<view class="text-pink">
						<view class="text-cut">{{person.name}}</view>
						<view class="city">({{person.yearBreath}} - {{person.yearDeath}})</view>
					</view>
					<view class="text-gray text-sm flex">
						<view class="text-cut">{{person.intro}}</view>
					</view>
				</view>
				<view class="action">
					<view class="text-grey text-xs">{{person.city}}</view>
					<!-- <view class="cu-tag round bg-red sm">5</view> -->
				</view>
			</view>


		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: [{
					id: 0,
					name: '用户',
					intro: '优秀的共产主义战士',
					yearBreath: 1900,
					yearDeath: 2000,
					src: 'https://ossweb-img.qq.com/images/lol/img/champion/Morgana.png',
					city:'内蒙古包头'
				},{
					id: 1,
					name: '用户3333',
					intro: '优秀的共产主义战士',
					yearBreath: 1900,
					yearDeath: 2000,
					src: 'https://ossweb-img.qq.com/images/lol/img/champion/Morgana.png',city:'北京'
				},{
					id: 2,
					name: '用户',
					intro: '优秀的共产主义战士',
					yearBreath: 1900,
					yearDeath: 2000,
					src: 'https://ossweb-img.qq.com/images/lol/img/champion/Morgana.png',city:'内蒙古呼和浩特'
				}]
			}
		},
		methods: {
			gotoPersonPage(id){
				// console.log(id)
				uni.navigateTo({
					url:"/pages/jinian/single/single?id="+id
				})
			}
		}
	}
</script>

<style>
.city{
	margin-left: 35upx;
	color:#555555;
	font-size:27upx;
}
</style>
