<!--
 * @Author: your name
 * @Date: 2020-04-19 00:56:28
 * @LastEditTime: 2020-12-22 15:17:40
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \hm_shop\pages\contact\contact.vue
-->
<template>
	<view class="contact">
		<image class="img" src="https://ss2.bdstatic.com/70cFvnSh_Q1YnxGkpoWK1HF6hhy/it/u=2483518927,608217211&fm=26&gp=0.jpg"></image>
		<view class="info">
			<view @click="phone">联系电话：400-618-9090 ( 点击拨打 )</view>
			<view>校区地址：浙江省杭州市下沙经济开发区4号大街187号盛泰时代山都</view>
		</view>
		<map class="map" :longitude="longitude" :scale="scale" :latitude="latitude" :markers="markers"></map>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				longitude: 120.363172,
				latitude: 30.312212,
				scale: 13,
				markers:[
					{
						longitude: 120.363172,
						latitude: 30.312212,
						iconPath: '../../static/hmlogo.png',
						width: 30,
						height: 30
					}
				]
			}
		},
		methods: {
			phone() {
				uni.makePhoneCall({
					phoneNumber: '400-618-9090'
				})
			}
		}
	}
</script>

<style lang="scss">
.contact{
	.img{
		width: 750rpx;
		height: 320rpx;
	}
	.info{
		padding: 10rpx 20rpx;
		font-size: 30rpx;
		view{
			line-height: 80rpx;
			border-bottom: 1px solid #eee;
		}
	}
	
	.map{
		width: 750rpx;
		height: 750rpx;
	}
}
</style>
