<template>
	<view class="content">
		<image class="logo animate__animated animate__bounce" src="/static/logo.png"></image>
		<view>
			<text class="title" @tap="show =!show">{{title}}</text>
		</view>
		<view class="iconfont icon-weibiaoti-"></view>
		<swiper indicator-dots autoplay :interval="3000" :duration="1000">
			<swiper-item>
				<view class="swiper-item">
					<img src="../../static/images/demo/demo4.jpg"
					lazy-load
					style="height: 350upx"
					>
				</view>
			</swiper-item>
		</swiper>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'cart2',
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
