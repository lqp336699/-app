<template>
	<view>
		<view class="flex align-center  mb-4" >
				<view class="flex align-center  justify-between rounded-circle px-1 ml-2" style="background-image: linear-gradient(to right, #528 , #3aa4f1); width:300rpx;height:90rpx">
					<view class="flex">
						<image class="rounded-circle" style="width:75rpx;height:75rpx;" :src="Data.avator" mode=""></image>
						<view class="flex flex-column ml-1">
							<text class="text-white">{{Data.username}}</text>
							<text class="font-sm text-white">送{{Data.gift_name}}</text>
						</view>				  									  							 
					</view>
					<view class="">
						<image style="width:75rpx;height:75rpx;" :src="Data.gift_image" mode=""></image>
					</view>				
				</view>
				<view>
					<text class="ml-2 font-lg text-warning">X {{Data.num}}</text>
				</view>							  			  
		</view>	
	</view>
</template>

<script>
	export default{
		props:{
			Data:{
				username:"11",
				avator:"../../static/default.jpg",
				gift_name:"22",
				gift_image:'../../static/gift/1.png',
				num:1	
			},
		},
		data(){
			return{
				
			}
		}
	}
</script>

<style>
</style>
