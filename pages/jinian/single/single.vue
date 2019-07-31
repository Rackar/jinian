<template>
	<view>
		<!-- {{id}} -->
		<!-- <view class="padding"> -->
		<view class="flex  padding justify-center">
			<view class="cu-avatar xxl round " style="background-image:url(https://ossweb-img.qq.com/images/lol/web201310/skin/big10001.jpg)"></view>

		</view>
		<view class="flex  padding justify-center">
			<view class="">
				{{person.name}}
			</view>
			<view class="">
				({{person.yearBreath}} - {{person.yearDeath}})
			</view>

		</view>
		<view class="padding text-center">
			<view class="padding radius shadow bg-white">简介
				<view class="intro">
					{{person.intro}}
				</view>
			</view>
		</view>

		<!-- <view class="padding text-left">
			<view v-for="(article,index) in articles" :key="index">
				{{index+1}}.{{article.title}} {{article.writer}} {{article.time}} 
			</view>
			</view> -->
		<view class="flex  p-xs margin-bottom-sm mb-sm">
			<view class="flex-sub  padding-xs margin-xs margin-left radius">
				<button class="cu-btn round" :class="['bg-' + 'cyan' , 'shadow']">亲人</button>
				<view class="cu-avatar round lg margin-xs" v-for="(item,index) in avatar" :key="index" :style="[{ backgroundImage:'url(' + avatar[index] + ')' }]">
				</view>
			</view>
			<view class="flex-treble  padding-xs margin-xs radius">
				<button class="cu-btn round" :class="['bg-' + 'cyan' , 'shadow']">文章</button>
				<view v-for="(article,index) in articles" :key="index">
					{{index+1}}.{{article.title}} {{article.writer}} {{article.time}}
				</view>
			</view>
		</view>
		<view class="flex  p-xs margin-bottom-sm mb-sm">
			<button class="cu-btn round margin-left-sm" :class="['bg-' + 'cyan' , 'shadow']">发表</button>
			<button class="cu-btn round margin-left-sm" :class="['bg-' + 'cyan' , 'shadow']">照片</button>
			<button class="cu-btn round margin-left-sm" :class="['bg-' + 'cyan' , 'shadow']">编辑</button>
			<button class="cu-btn round margin-left-sm " :class="['bg-' + 'cyan' , 'shadow']">分享</button>
			<button class="cu-btn round margin-left-sm" :class="['bg-' + 'cyan' , 'shadow']">投诉</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				id: 0,
				person: {
					id: 0,
					name: '用户',
					intro: '优秀的共产主义战士',
					yearBreath: 1900,
					yearDeath: 2000,
					src: 'https://ossweb-img.qq.com/images/lol/img/champion/Morgana.png',
					city: '内蒙古包头'
				},
				articles: [{
						id: 0,
						title: '纪念母亲',
						writer: '老大',
						time: '2019'
					},
					{
						id: 0,
						title: '在高考的那一年里',
						writer: '老二',
						time: '2016'
					},
					{
						id: 0,
						title: '在高考的那一年里',
						writer: '老二',
						time: '2016'
					},
					{
						id: 0,
						title: '在高考的那一年里',
						writer: '老二',
						time: '2016'
					},
					{
						id: 0,
						title: '在高考的那一年里',
						writer: '老二',
						time: '2016'
					},
					{
						id: 0,
						title: '在高考的那一年里',
						writer: '老二',
						time: '2016'
					},
					{
						id: 0,
						title: '在高考的那一年里',
						writer: '老二',
						time: '2016'
					},
					{
						id: 0,
						title: '在高考的那一年里',
						writer: '老二',
						time: '2016'
					}
				],
				avatar: [
					'https://ossweb-img.qq.com/images/lol/web201310/skin/big10001.jpg',
					'https://ossweb-img.qq.com/images/lol/web201310/skin/big81005.jpg',
					'https://ossweb-img.qq.com/images/lol/web201310/skin/big25002.jpg'
				]
			}
		},
		onLoad(option) {
			console.log(option.id); //打印出上个页面传递的参数。

			this.getSingleInfo(option.id)
		},
		methods: {
			getSingleInfo(id) {
				this.id = id
			}
		}
	}
</script>

<style>
	.intro {
		height: 140upx;
	}
</style>
