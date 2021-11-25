<template>
	<view class="pagea flex">
		<!-- <video class="flex-1" src="http://192.168.1.6:23481/live/CeeOuEkOsZ9fKVU7VAbh.flv?sign=1600799741-2f1403bbde3bea91f606b84f3ded5544" autoplay :controls="false"></video> -->
		<view class="bg-danger" 
			  style="height:120rpx; position:fixed; bottom:0; left:0;right:0;" 
		      >
		</view>
		<!-- 头部 -->
		<view style="height:80rpx; position:fixed;left:0;bottom:0; right:0;" 
			  class="bg-danger" 
			  :style="'top:'+statusBarHeight+'px'"
			  >
			  <!-- 头部 -->
			  <view class="bg-primary flex justify-between">
				  <view style="width:325rpx;box-sizing:border-box;" class=" flex justify-between px-3">
					  <view class="">
						<image style="width:75rpx;height:75rpx;" src="../../static/gift/1.png" mode=""></image>  
					  </view>
					  <view class="">
						  <image style="width:75rpx;height:75rpx;" src="../../static/gift/1.png" mode=""></image>
					  </view>
				  </view>
				  <view style="width:325rpx;box-sizing:border-box;" class="rounded-circle flex justify-between">
				  		<view class="">
				  			<image style="width:75rpx;height:75rpx;" src="../../static/gift/1.png" mode=""></image>  
				  		</view>
				  		<view class="rounded-circle  bg-danger" >
				  			<text class="text-white font-sm text-center" style="line-height:75rpx; display:block; width:75rpx;height:75rpx;">100</text>
				  		</view>			  
				  </view>
			  </view>
			  <!-- 金币 -->
			 <view class="rounded-circle ml-2" style="width:250rpx; height:50rpx; background-color: rgba(0,0,0,0.1);">
				  <text class="text-warning mr-2 ml-4">金币</text>
				  <text>0</text>
			  </view>
			  
			  <!-- 收到礼物 -->
		<view>
			  <scroll-view class="mt-5"  scroll-with-animation="true"  scroll-y="true" show-scrollbar="false" style="width:450rpx; height:450rpx">
				  <view v-for="item in Data">
					  <fgift :Data="item"></fgift>
				  </view>
			  </scroll-view>
		</view>
	</view>
</template>

<script>
	import fgift from '@/components/f-gift.vue';
	export default {
		components:{fgift},
		data() {
			return {
				statusBarHeight:0,
				Data:[{
					username:"发送人",
					avator:"../../static/default.jpg",
					gift_name:"蛋糕",
					gift_image:'../../static/gift/1.png',
					num:1,
				},
				{
					username:"发送人",
					avator:"../../static/default.jpg",
					gift_name:"蛋糕",
					gift_image:'../../static/gift/1.png',
					num:1		
				}]
			}
		},
		onLoad(){
			let res = uni.getSystemInfoSync({});
			console.log(res)
			this.statusBarHeight = res.statusBarHeight;
		},
		created(){
			let _this = this;
			setInterval(()=>{
				_this.Data.push({
					username:"发送人",
					avator:"../../static/default.jpg",
					gift_name:"蛋糕",
					gift_image:'../../static/gift/1.png',
					num:1
				})
			},3000)
		},
		methods: {
			
		}
	}
</script>

<style>
.pagea{
	flex:1;
	height: 100vh;
}	
</style>
