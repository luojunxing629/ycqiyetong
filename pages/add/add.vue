<template>
	<view class="container">
		<u-navbar
		title="发布需求"
		bgColor="transparent"
		leftIconColor="#fff"
		:titleStyle="{ color: '#fff' }"
		:autoBack="true"
		></u-navbar>
		<view class="navbar">
			<image class="navbar-img" src="../../static/index/navbarbackground.png"></image>
		</view>
		<view class="add-form-container">
			<view class="add-form-part1">		
					<text class="form-text">标题</text>
					<view class="form-input">
					<u--input
						placeholder="请填写"
						inputAlign="right"
						fontSize="36rpx"
					    border="none"
					    v-model="value"
					    @change="change"
					></u--input>
					</view>
			</view>
			<view class="add-form-part1">
				<text class="form-text">数量</text>
				<view class="form-input">
				<u--input
					placeholder="请填写"
					inputAlign="right"
					fontSize="36rpx"
				    border="none"
				    v-model="value"
				    @change="change"
				></u--input>
				</view>		
			</view>
			<view class="add-form-part2">
				<text class="form-text">标题</text>
				<view class="form-input">
					<u--input
						placeholder="例如: 个"
						inputAlign="right"
						fontSize="36rpx"
					    border="none"
					    v-model="value"
					    @change="change"
					></u--input>
					</view>
			</view>
			<view class="add-form-part1">
				<text class="form-text">需求地</text>
				<view class="form-input">
				<u--input
					placeholder="请填写"
					inputAlign="right"
					fontSize="36rpx"
				    border="none"
				    v-model="value"
				    @change="change"
				></u--input>
				</view>		
			</view>
			<view class="add-form-part2">
				<text class="form-text">有效时间</text>
				<view class="form-input">
					<u--input
						placeholder="请选择"
						inputAlign="right"
						fontSize="36rpx"
					    border="none"
					    v-model="value"
					    @change="change"
					></u--input>
					</view>
			</view>
			
			<view class="add-form-textarea">
				<text class="form-text">需求描述</text>
				<view class="form-textarea">
					<u--textarea v-model="value1" fontSize="36rpx" placeholder="请描述" border="none"></u--textarea>
				</view>
			</view>
			
			<view class="add-form-danger">
				<text class="form-text">是否紧急</text>
				<u-switch v-model="value" @change="change"></u-switch>
			</view>
			<view class="add-form-unload">
				<text class="form-text">上传图片</text>
				<u-upload
					:fileList="fileList1"
					@afterRead="afterRead"
					@delete="deletePic"
					name="1"
					multiple
					:maxCount="10"
				></u-upload>
			</view>
			<view class="add-form-submit">
				<u-button text="提交" size="large" shape="circle" color="rgba(16, 203, 225, 1)"></u-button>
			</view>
			<view class="bottom-bg"></view>
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

<style lang="scss" scoped>
/deep/.uni-textarea-wrapper {
	background-color: rgba(240, 244, 247, 1);
}
.navbar-img {
	width: 100%;
	height: 100rpx;
}
.container {
	height: 100%;
	background-color: rgba(240, 244, 247, 1);
}
.form-input {
	width: 30%;
}
.form-text {
	font-size: 36rpx;
	font-weight: 550;
}
.add-form-part1 {
	background-color: #fff;
	margin: 20rpx 20rpx 0rpx 20rpx;
	height: 70rpx;
	padding: 20rpx 20rpx 20rpx 20rpx;
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	align-items: center;
	border-bottom: 1rpx solid rgba(210, 210, 216, 1.0);
}
.add-form-part2 {
	background-color: #fff;
	margin: 0rpx 20rpx 20rpx 20rpx;
	height: 70rpx;
	padding: 20rpx 20rpx 20rpx 20rpx;
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	align-items: center;
}
.form-textarea {
	width: 80%;
	margin: auto;
}
.add-form-textarea {
	background-color: #fff;
	display: flex;
	flex-direction: column;
	margin: 20rpx 20rpx 0rpx 20rpx;
	padding: 20rpx 0 20rpx 0;
	text{
		margin-left: 20rpx;
		margin-bottom: 20rpx;
	}
}
.add-form-danger {
	background-color: #fff;
	margin: 20rpx 20rpx 0rpx 20rpx;
	height: 70rpx;
	padding: 20rpx 20rpx 20rpx 20rpx;
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	align-items: center;
}
.add-form-unload {
	background-color: #fff;
	margin: 20rpx 20rpx 50rpx 20rpx;
	padding: 20rpx 20rpx 20rpx 20rpx;
	display: flex;
	flex-direction: column;
	text{
		margin-bottom: 30rpx;
	}
}
.add-form-submit {
	margin: auto;
	width: 70%;
}
.bottom-bg {
	height: 90rpx;
	background-color: rgba(240, 244, 247, 1);
}
</style>
