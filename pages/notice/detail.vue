<template>
	<view class="container">
		<u-navbar
		title="公告详情"
		bgColor="transparent"
		leftIconColor="#fff"
		:titleStyle="{ color: '#fff' }"
		:autoBack="true"
		></u-navbar>
		<view class="navbar">
			<image class="navbar-img" src="../../static/index/navbarbackground.png"></image>
		</view>
		<view class="detail-container">
			<view class="title-container">
				<text class="detail-title">{{detail.title}}</text>
				<text class="detail-title-source">【 来源： {{detail.creater}} 】</text>
				<text class="detail-title-time">{{detail.createtime}}</text>
			</view>
			<view class="content-container">
				<text class="detail-content">{{detail.content}}</text>
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
			detail:{
				title:'扬州疫情防控2022年第126号通告', creater:'扬州新冠疫情防控指挥部', createtime:'2022-06-01', content:'截至5月6日24时，本轮仪征疫情已发现45名无症状感染者，其中，仪征市41人，扬州市经济技术开发区4人（新集镇关联病例），主要集中在新集镇江宁村和威立安服装厂。45名无症状感染者均已送至扬州市第三人民医院，正在受到妥善的医疗救治和隔离观察，病情均平稳。'
			}
		}
		methods: {
			
		}
	}
	}
</script>

<style lang="scss" scoped>

.navbar-img {
	width: 100%;
	height: 100rpx;
}
.detail-container {
	display: flex;
	flex-direction: column;
	margin: 40rpx;
}
.title-container {
	display: flex;
	flex-direction: column;
}
.detail-title {
	font-size: 36rpx;
	font-weight: 550;
	margin-bottom: 20rpx;
}
.detail-title-source {
	font-size: 30rpx;
	color: rgba(155, 155, 155, 1);
	margin-bottom: 20rpx;
}
.detail-title-time {
	font-size: 30rpx;
	color: rgba(155, 155, 155, 1);
}
.content-container {
	margin-top: 30rpx;
	font-size: 30rpx;
	line-height: 50rpx;
}
</style>
