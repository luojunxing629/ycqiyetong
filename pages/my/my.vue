<template>
	<view class="container">
		<view class="navbar">
			<image class="navbar-img" src="../../static/index/navbarbackground.png"></image>
		</view>
		<view class="container2">
			<view class="card-container">
				<view class="card">
					<image class="avatar" src="../../static/my/登录头像.png"></image>
					<text class="login-status">暂未登录</text>
					<u-button :plain="true" shape="circle" color="rgba(16, 203, 225, 1)" text="登录/注册"></u-button>
				</view>
			</view>
			<view class="options">
				<view class="option-item">
					<image class="options-img" src="../../static/my/个人信息.png"></image>
					<text class="options-text">个人信息</text>
				</view>
				<view class="option-item">
					<image class="options-img" src="../../static/my/联系记录.png"></image>
					<text class="options-text">联系记录</text>
				</view>
				<view class="option-item">
					<image class="options-img" src="../../static/my/我的发布.png"></image>
					<text class="options-text">我的发布</text>
				</view>
				<view class="option-item">
					<image class="options-img" src="../../static/my/关于扬链通.png"></image>
					<text class="options-text">关于扬链通</text>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
.container {
	height: 100%;
	background-color: rgba(240, 244, 247, 1);
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
.container2 {
	background-color: rgba(240, 244, 247, 1);
/* 	padding: 0 20rpx 50rpx 20rpx; */
	margin: 0 20rpx 0 20rpx;
}
.card-container {
	width: 98%;
	margin:-50rpx 10rpx 20rpx 10rpx;
	background-color: #fff;
	align-content: center;
	position: relative;
}
.card {
	width: 200rpx;
	margin: auto;
	padding-bottom: 40rpx;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	background-color: #fff;

}
.avatar {
	margin-top: -80rpx;
	margin-bottom: 30rpx;
	width: 70%;
	height: 150rpx;
}
.login-status {
	margin-bottom: 20rpx;
}
.options {
	display: flex;
	width: 98%;
	margin-left: 10rpx;
	margin-right: 10rpx;
	padding-bottom:200rpx;
	flex-direction: column;
	background-color: #fff;
}
.option-item {
	border-bottom: 1rpx solid rgba(228, 228, 228, 1);
	height: 100rpx;
	width: 90%;
	margin: auto;
	display: flex;
	flex-direction: row;
	justify-content: left;
	align-items: center;
}
.options-img {
	width: 50rpx;
	height: 50rpx;
	margin-left: 20rpx;
	margin-right: 20rpx;
}
</style>
