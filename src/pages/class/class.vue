<template>
	<view class="content">
		<image class="logo animate__animated animate__bounce" src="/static/logo.png"></image>
		<view>
			<text class="title" @tap="show =!show">{{title}}</text>
		</view>
		<view class="iconfont icon-weibiaoti-"></view>
		<!-- 滚动 -->
		<scroll-view scroll-x class="scroll-row">
			<view style="width: 200upx" class="border scroll-row-item">1</view>
			<view style="width: 200upx" class="border scroll-row-item">2</view>
			<view style="width: 200upx" class="border scroll-row-item">3</view>
			<view style="width: 200upx" class="border scroll-row-item">4</view>
			<view style="width: 200upx" class="border scroll-row-item">5</view>
		</scroll-view>
		<!-- 栅格布局 -->
		<view class="row p-2 text-center" style="width: 100%; ">
			<view class="span-4 py-2">
				<view class="iconfont icon-weibiaoti-"></view>
				1
			</view>
			<view class="span-4 py-2">
				<view class="iconfont icon-weibiaoti-"></view>
				2
			</view>
			<view class="span-4 py-2">
				<view class="iconfont icon-weibiaoti-"></view>
				3
			</view>
			<view class="span-4 py-2">
				<view class="iconfont icon-weibiaoti-"></view>
				4
			</view>
			<view class="span-4 py-2">
				<view class="iconfont icon-weibiaoti-"></view>
				5
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'class',
				show: false
			}
		},
		onLoad() {
			
		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin: 200rpx auto 50rpx auto;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
