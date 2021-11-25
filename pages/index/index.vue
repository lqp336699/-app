<template>
	<view class="">
		<swiper style="height:250rpx" :indicator-dots="true" :autoplay="true" :interval="3000" :duration="200">
			<swiper-item>
				<image src="../../static/banner/1.jpg" mode="" style="width:750rpx;height:250rpx;"></image>
			</swiper-item>
			<swiper-item>
				<image src="../../static/banner/2.jpg" mode="" style="width:750rpx;height:250rpx;"></image>
			</swiper-item>
		</swiper>
		<view class="flex flex-wrap" >
			<view v-for="i in 10" @click="openlive" class="" style="box-sizing:border-box width:360rpx; height:365rpx; padding:5rpx; position: relative;">
				<image style="width:365rpx;height:365rpx;" src="../../static/1.jpg" mode="aspectFill" class="rounded"></image>
				<view class="rounded-circle px-2 flex  align-center" style="background-color: rgba(0,0,0,0.4); position:absolute; top: 15rpx; left: 15rpx;">
					<text class="iconfont mr-1" style="color:yellow">&#xec80;</text>
					<text class="text-white">0</text>
				</view>
				<view class="rounded-circle px-2 flex  align-center" style="background-color: rgba(0,0,0,0.4); position:absolute; top: 15rpx; right: 15rpx;">
					<text class=" text-white mr-1 font">人气:</text>
					<text class="text-white ">0</text>
				</view>
				<view class="rounded-circle flex  align-center" style=" position:absolute; bottom: 15rpx; left: 15rpx;">
					<text class="text-white">标题</text>
				</view>
				<view class="rounded-circle px-2 flex  align-center" style="background-color: rgba(0,0,0,0.4); position:absolute; bottom: 15rpx; right: 15rpx;">
					<text class="bg-danger rounded-circle mr-1" style="width: 20rpx; height: 20rpx;"></text>
					<text class="text-white">已结束</text>
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
		onLoad() {

		},
		methods: {
			openlive(){
				uni.navigateTo({
					url:"../live/live",
					success:res => {},
					fail:()=>{},
					complete:()=>{}
				})
			}
		}
	}
</script>

<style>
	
</style>
