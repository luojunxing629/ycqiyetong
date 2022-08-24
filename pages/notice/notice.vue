<template>
	<view class="container">
		<u-navbar
		title="公告"
		bgColor="transparent"
		leftIconColor="#fff"
		:titleStyle="{ color: '#fff' }"
		:autoBack="true"
		></u-navbar>
		<view class="navbar">
			<image class="navbar-img" src="../../static/index/navbarbackground.png"></image>
		</view>
		<view class="notice-container">
		<view class="notice-list-container" v-for="(item,index) in noticeList" :key="index" @click="handleDetail()">
			<view class="notice-list-title-circle" v-if="item.isTop == 1"></view>
			<view class="notice-list-title-circle2" v-if="item.isTop == 0"></view>
			<view class="notice-list-title">
				<text class="notice-list-title-text">{{item.title}}</text>
				<text class="notice-list-time">发布日期： {{item.time}}</text>
			</view>
			
		</view>
		</view>
	</view>
</template>

<script>
	export default {
		onShow() {
			uni.hideTabBar()
		},
		data() {
			return {
			noticeList:[
				{isTop:'1', title:'扬州疫情防控2022年第126号通告', time:'2022-06-01' },
				{isTop:'1', title:'扬州疫情防控2022年第126号通告', time:'2022-06-01' },
				{isTop:'1', title:'扬州疫情防控2022年第126号通告', time:'2022-06-01' },
				{isTop:'0', title:'扬州疫情防控2022年第126号通告疫情防控2022年第126号通告', time:'2022-06-01' },
				{isTop:'0', title:'扬州疫情防控2022年第126号通告疫情防控空2022年第126号通告', time:'2022-06-01' },
				{isTop:'0', title:'扬州疫情防控2022年第126号通告', time:'2022-06-01' }
			]
			}
		},
		methods: {
			handleDetail() {
				uni.navigateTo({
					url:'./detail'
				})
			}
		}
	}
</script>

<style lang="scss" scoped>

.navbar-img {
	width: 100%;
	height: 100rpx;
}
.notice-container {
	padding: 20rpx 20rpx 20rpx 20rpx;
}
.notice-list-container {
	display: flex;
	flex-direction: row;
	justify-content: left;
	padding: 30rpx 0 30rpx 0;
	border-bottom: 1rpx solid rgba(155, 155, 155, 1);
}
.notice-list-title {
	display: flex;
	flex-direction: column;
}
.notice-list-title-text {
	font-size: 34rpx;
	font-weight: 550;
	margin-bottom: 20rpx;
}
.notice-list-time {
	font-size: 28rpx;
	color: rgba(155, 155, 155, 1);
}
.notice-list-title-circle {
	width: 20rpx;
	height: 20rpx;
	margin: 10rpx 40rpx 0 20rpx;
	background-color: rgba(16, 203, 225, 1);
	border-radius: 50%;
}
.notice-list-title-circle2 {
	width: 20rpx;
	height: 20rpx;
	margin: 10rpx 40rpx 0 20rpx;
	background-color: #fff;
	border-radius: 50%;
}
</style>
