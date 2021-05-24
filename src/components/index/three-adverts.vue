<template>
	<view class="d-flex" style="box-sizing: border-box!important;display: flex">
		<view class="col-6 d-flex a-stretch" style="width: 373upx;">
			<image style="height: 530upx;width: 373upx;"
			:src="resdata.big.src"></image>
		</view>
		<view class="col-6 d-flex flex-column j-sb">
			<image style="height: 260upx;width: 375upx"
			:src="resdata.smalltop.src"
			mode="widthFix"></image>
			<image style="height: 260upx;width: 375upx"
			:src="resdata.smallbottom.src"
			mode="widthFix"></image>
		</view>
	</view>
</template>

<script>
	export default {
		props:{
			resdata:Object
		}
	}
</script>

<style>
</style>
