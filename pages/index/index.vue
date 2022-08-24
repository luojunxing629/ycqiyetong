<template>
	<view class="container">
		<view class="navbar">
			<image class="navbar-img" src="../../static/index/navbarbackground.png"></image>
		</view>
		<view class="container2">
			<image class="big-img" src="../../static/index/扬城企业通.png"></image>
		<view class="notice-container">
			<view style="align-items: center;display: flex;flex-direction: row;">
			<image class="notice-img" src="../../static/index/notice.png"></image>
			<text class="notice-text">扬州市疫情发布</text>
			</view>
			<text class="more" @click="handleMore()">更多>></text>
		</view>
		<view class="grid-container">
			<u-grid :border="false" col="5"  >
				<u-grid-item class="list-container" v-for="(item,index) in navlist" :key="index">
					<image class="list-img" :src="item.url" />
					<text class="list-title">{{item.title}}</text>
				</u-grid-item>
			</u-grid>
		</view>
		<view class="supply-need-wrap">
		<view class="search-container">
			<text class="search-title">供需对接</text>
			<view class="search-bar">
			<u-search placeholder="请输入关键字" height="80rpx" inputAlign="right" searchIcon="" shape="round" :showAction='false'></u-search>
			</view>
		</view>
		
		</view>
		<view class="example-container">
			<view class="example-supply" v-for="(item,index) in exampleSupply" :key="index">
				<view class="example-title">
					<view class="button-wrap" style="height: 25rpx;">
					<u-button text="供方" size="medium" color="rgba(90, 179, 244, 1)" ></u-button>
					</view>
					<view class="example-title-text">{{item.titletext}}</view>
				</view>
				<view class="example-detail">
					<u-grid col="3">
						<u-grid-item class="example-detail-grid">
							<text class="example-detail-grid-imformation">{{item.number}}台</text>
							<text class="example-detail-grid-information-attribute">数量</text>
						</u-grid-item>
						<u-grid-item class="example-detail-grid">
							<text class="example-detail-grid-imformation">{{item.type}}</text>
							<text class="example-detail-grid-information-attribute">类型</text>
						</u-grid-item>
						<u-grid-item class="example-detail-grid">
							<text class="example-detail-grid-imformation">{{item.source}}</text>
							<text class="example-detail-grid-information-attribute">来源</text>
						</u-grid-item>
					</u-grid>
				</view>
			</view>
			
			<view class="example-supply" v-for="(item,index) in exampleNeed" :key="index">
				<view class="example-title">
					<view class="button-wrap" style="height: 25rpx;">
					<u-button text="需方" size="medium" color="rgba(255, 116, 0, 1)"></u-button>
					</view>
					<view class="example-title-text">{{item.titletext}}</view>
				</view>
				<view class="example-detail">
					<u-grid col="3">
						<u-grid-item class="example-detail-grid">
							<text class="example-detail-grid-imformation">{{item.number}}台</text>
							<text class="example-detail-grid-information-attribute">数量</text>
						</u-grid-item>
						<u-grid-item class="example-detail-grid">
							<text class="example-detail-grid-imformation">{{item.type}}</text>
							<text class="example-detail-grid-information-attribute">类型</text>
						</u-grid-item>
						<u-grid-item class="example-detail-grid">
							<text class="example-detail-grid-imformation">{{item.source}}</text>
							<text class="example-detail-grid-information-attribute">来源</text>
						</u-grid-item>
					</u-grid>
				</view>
			</view>
		</view>
		
		</view>
	</view>
</template>

<script>
	export default {
		
		data() {
			return {
				title: 'Hello',
				navlist:[
					{title:'产品物资', url:'../../static/index/产品物资.png'},
					{title:'原料耗材', url:'../../static/index/原料耗材.png'},
					{title:'元器件', url:'../../static/index/元器件.png'},
					{title:'物流配送', url:'../../static/index/物流配送.png'},
					{title:'工业软件', url:'../../static/index/工业软件.png'},
					{title:'人才招聘', url:'../../static/index/人才招聘.png'},
					{title:'项目核算', url:'../../static/index/项目核算.png'},
					{title:'供应链', url:'../../static/index/供应链.png'},
					{title:'企业服务', url:'../../static/index/企业服务.png'},
					{title:'数据报表', url:'../../static/index/数据报表.png'},
				],
				exampleSupply:[
					{titletext:'ABB变频器，EMC滤波器2类环境 （接地） ACS880-01-07A6-5+E200', number:'500', type:'元器件', source:'工品行'},
				],
				exampleNeed:[
					{titletext:'ABB变频器，EMC滤波器2类环境 （接地） ACS880-01-07A6-5+E200', number:'500', type:'元器件', source:'工品行'}
				]
			}
		},
		onLoad() {

		},
		
		methods: {
			handleMore() {
				uni.navigateTo({
					url:'../notice/notice'
				})
			}
		}
	}
</script>

<style lang="scss" scoped>
/deep/ .u-search__content {
	height: 70rpx;
}
/deep/ .u-button {
	height: 40rpx;
	width: 120rpx;
	border-radius: 0;
}
.container {
	height: 100%;
	background-color: rgba(240, 244, 247, 1);
}
.container2 {
	background-color: rgba(240, 244, 247, 1);
	padding: 0 20rpx 50rpx 20rpx;
}
.navbar {
	height: 300rpx;
	position: relative;
	width: 100%;
}
.navbar-img {
	position: absolute;
	    width: 100%;
	    height: 300rpx;
	    top: 0;
	    left: 0;
}
.big-img {
	position: absolute;
	width: 95%;
	height: 250rpx;
	top: 12%;
	left: 2.5%;

}
.notice-container {
	height: 90rpx;
	margin-top: 150rpx;
	padding: 0rpx 30rpx 0 30rpx;
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	background-color: #fff;
	align-items: center;
}
.notice-img {
	height: 50rpx;
	width: 100rpx;
	margin-right: 30rpx;
}
.notice-text {
	font-size: 28rpx;
}
.more {
	font-size: 28rpx;
	color: rgba(90, 179, 244, 1);
}
.grid-container {
	background-color: #fff;
	padding: 20rpx;
	margin-top: 20rpx;
}
.list-container {
	margin: 30rpx 0 30rpx 0;
}
.list-img {
	width: 50rpx;
	height: 50rpx;
	margin-bottom: 20rpx;
}
.list-title {
	font-size: 25rpx;
}
.supply-need-wrap {
	background-color: #fff;
}
.search-container {
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	background-color: #fff;
	margin-top: 20rpx;
	padding:0 30rpx 0 30rpx;
	height: 100rpx;
	align-items: center;
}
.search-bar {
	width: 400rpx;
}
.search-title {
	font-size: 35rpx;
	font-weight: 700;
}
.example-container {
	background-color: #fff;
	
}

.example-title {
	display: flex;
	flex-direction: row;
	margin-bottom: 30rpx;
}
.example-title-text {
	font-size: 33rpx;
	font-weight: 700;
}
.example-detail-grid-imformation {
	font-size: 28rpx;
}
.example-detail-grid-information-attribute {
	font-size: 26rpx;
	color: rgba(184, 182, 182, 1);
}
</style>
