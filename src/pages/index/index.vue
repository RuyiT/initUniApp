<template>
	<view>
		<!-- <image class="logo animate__animated animate__bounce" src="/static/logo.png"></image>
		<view>
			<text class="title" @tap="show =!show">{{title}}</text>
		</view>
		<view class="iconfont icon-weibiaoti-"></view> -->

	<!-- 轮播图组件 -->
	<swiperImage :resdata="swipers"></swiperImage>

	<!-- 轮播图组件 -->
	<view class="row j-center text-center m-2">
		<block v-for="(item,idx) in indexnavs" :key="idx">
			<view class="span-4 d-flex flex-column j-center a-center py-1">
				<image
					:src="item.src"
					style="width: 60upx;height: 60upx"
					mode="widthFix"
				/>
				<text class="font-sm">{{item.text}}</text>
			</view>
		</block>
	</view>

	<!-- 全局分割线 -->
	<divider></divider>

	<!-- 三图广告位 -->
	<view class="d-flex">
		<image style="height: 530upx;width: 373upx;border-right: 2upx solid #f5f5f5"
			lazy-load
			src="/static/images/demo/demo1.jpg">
		</image>
		<view class="d-flex flex-column">
			<image style="height: 264upx;width: 375upx;border-right: 2upx solid #f5f5f5"
			src="/static/images/demo/demo2.jpg"
			mode="widthFix"></image>
			<image style="height: 264upx;width: 375upx;border-right: 2upx solid #f5f5f5"
			src="/static/images/demo/demo3.jpg"
			mode="widthFix"></image>
		</view>
	</view>
	<threeAdverts :resdata="threeAdv"></threeAdverts>

	<!-- 购物车  style里的bottom: 50px是为了pc端调试能看到,学习的时候才加上 -->
	<view class="bg-white border-top position-fixed left-0 bottom-0 right-0 d-flex a-stretch" style="height: 100upx; bottom: 50px">
		<view class="flex-1 d-flex flex-column a-center j-center line-h-md">
			<view class="iconfont icon-like-fill line-h font-md">
				收藏
			</view>
		</view>
		<view class="flex-1 d-flex flex-column j-center a-center line-h-md">
			<view class="iconfont icon-gouwuchekong line-h font-md">
				购物车
			</view>
		</view>
		<view style="flex: 2.5" hover-class="main-bg-hover-color" class="text-white main-bg-color d-flex j-center a-center font-md">
			加入购物车
		</view>
	</view>	
	</view>
</template>

<script>
import swiperImage from "@/components/index/swiper-image.vue";
import indexNav from "@/components/index/index-nav.vue";
import threeAdverts from "@/components/index/three-adverts.vue";
	// import card from "@/components/common/card.vue";
	export default {
		components: {
			swiperImage,
			indexNav,
			threeAdverts
		},
		data() {
			return {
				title: 'Hello',
				show: false,
				swipers: [
					{
						src: "../../static/images/demo/demo4.jpg"
					},{
						src: "../../static/images/demo/demo4.jpg"
					},{
						src: "../../static/images/demo/demo4.jpg"
					}
				],
				indexnavs: [
					{
						src: "/static/indexnav/1.png",
						text: "新品发布"
					},
					{
						src: "/static/indexnav/2.gif",
						text: "小米众筹"
					},
					{
						src: "/static/indexnav/3.gif",
						text: "依旧换新"
					},
					{
						src: "/static/indexnav/4.gif",
						text: "一分换团"
					},
					{
						src: "/static/indexnav/5.gif",
						text: "超值特卖"
					},
					{
						src: "/static/indexnav/6.gif",
						text: "小米秒杀"
					},
					{
						src: "/static/indexnav/7.gif",
						text: "真心想要"
					},
					{
						src: "/static/indexnav/8.gif",
						text: "电视热卖"
					},
					{
						src: "/static/indexnav/9.gif",
						text: "家电热卖"
					},
					{
						src: "/static/indexnav/10.gif",
						text: "米粉卡"
					}
				],
				threeAdv: {
					big: {
						src: "/static/images/demo/demo1.jpg"
					},
					smalltop: {
						src: "/static/images/demo/demo2.jpg"
					},
					smallbottom: {
						src: "/static/images/demo/demo3.jpg"
					},
				}
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
