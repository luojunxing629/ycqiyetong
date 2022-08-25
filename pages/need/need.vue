<template>
	<view class="container">
		<u-navbar
		title="需求"
		bgColor="transparent"
		leftIconColor="#fff"
		:titleStyle="{ color: '#fff' }"
		:autoBack="true"
		></u-navbar>
		<view class="navbar">
			<image class="navbar-img" src="../../static/index/navbarbackground.png"></image>
		</view>
		<view class="u-tabs-container">
			<u-tabs :list="options" @click="handleTabschange(index)"></u-tabs>
		</view>
		<view class="example-container">
			<view class="example-supply" v-for="(item,index) in exampleNeed" :key="index">
				<view class="example-title">
					<view class="button-wrap">
					<u-button text="需方" size="medium" color="rgba(255, 116, 0, 1)" ></u-button>
					</view>
					<view class="example-title-text">{{item.titletext}}</view>
				</view>
				<view class="example-time">
					<view v-if="item.isDanger == 1"  class="button-container" style="width:10rpx;">
					<u-button text="紧急" size="mini" color="linear-gradient(to right,rgba(255, 0, 0, 1),rgba(255, 118, 0, 1))"  ></u-button>
					</view>
					
					<text class="example-time-line">有效期： {{item.effectiveTime}}</text>
					<text class="example-time-detail">详情>></text>
				</view>
				<view class="line-container" style="width: 90%;padding: 30rpx 20rpx 20rpx 20rpx;margin: auto;">
				<u-line color="rgba(208, 210, 216, 1.0)" ></u-line>
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
</template>

<script>
	export default {
		data() {
			return {
				option:'',
				options:[
					{name:'全部'},{name:'产品物资'},{name:'原料耗材'},{name:'元器件'},{name:'零部件'},{name:'工业'}
				],
				exampleSupply:[
					{titletext:'ABB变频器，EMC滤波器2类环境 （接地） ACS880-01-07A6-5+E200', number:'500', type:'元器件', source:'工品行',effectiveTime:'2022-12-31'},
					{titletext:'ABB变频器，EMC滤波器2类环境 （接地） ACS880-01-07A6-5+E200', number:'500', type:'元器件', source:'工品行',effectiveTime:'2022-12-31'},
				],
				exampleNeed:[
					{titletext:'ABB变频器，EMC滤波器2类环境 （接地） ACS880-01-07A6-5+E200', number:'500', type:'元器件', source:'工品行',effectiveTime:'2022-12-31',isDanger:'1'},
					{titletext:'ABB变频器，EMC滤波器2类环境 （接地） ACS880-01-07A6-5+E200', number:'500', type:'元器件', source:'工品行',effectiveTime:'2022-12-31',isDanger:'0'},
					{titletext:'ABB变频器，EMC滤波器2类环境', number:'500', type:'元器件', source:'工品行',effectiveTime:'2022-12-31',isDanger:'0'}
				]
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss" scoped>
.container {
	background-color: rgba(240, 244, 247, 1);
	padding-bottom: 20rpx;
}
.navbar-img {
	width: 100%;
	height: 100rpx;
}
.u-tabs-container {
	background-color: rgba(240, 244, 247, 1);
	margin-top: -10rpx;
}
.example-supply {
	margin-top: 30rpx;
	margin-bottom: 30rpx;
	background-color: #fff;
}
.example-container {
	background-color: rgba(233, 237, 239, 1.0);
}
.button-container {
	margin-left: 20rpx;
	margin-right: -130rpx;
}
</style>