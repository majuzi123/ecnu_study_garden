<template>
	<view class="container">
		<!-- 头像部分 -->
		<view class="header">
			<image src="../../static/index/index_discover/user_example.png" mode="widthFix">
			<view>用户一号</view>
		</view>
		<!-- 分区与标签 -->
		<view class="body1">
			<view class="body1Label">
				学习天地
			</view>
			<view class="body1Tag">
				#学习#打卡
			</view>
		</view>
		<!-- 内容简介 -->
		<view class="content">
			11111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111111
		</view>
		<!-- 互动 -->
		<view class="Interaction">
			<view class="">
				<image src="../../static/index/index_discover/commit.png" mode="widthFix">
				<view class="InteractionNum">900</view>
			</view>
			<view class="">
				<image src="../../static/index/index_discover/favour.png" mode="widthFix">
				<view class="InteractionNum">900</view>
			</view>
			<view class="">
				<image src="../../static/index/index_discover/collect.png" mode="widthFix">
				<view class="InteractionNum">900</view>
			</view>
		</view>
	</view>
</template>

<script>
	
	export default{
		name:'ForumItem',
		
	}
</script>

<style scoped>
	.container{
		margin: 15rpx 15rpx;
		background-color: white;
		padding: 1rpx 15rpx;
		border-radius: 20rpx;
	}
	.header{
		height: 80rpx;
	}
	.header image{
		width:80rpx;
		display: inline-block;
	}
	.header view{
		line-height: 40rpx;
		vertical-align: 26rpx;
		display: inline-block;
	}
	
	.body1{
		margin-top: 10rpx;
	}
	.body1Label{
		line-height: 50rpx;
		background-color: #ffcc00;
		color: white;
		width: 150rpx;
		text-align: center;
		border-radius: 50rpx;
		display: inline-block;
	}
	.body1Tag{
		margin-left: 50rpx;
		line-height: 50rpx;
		display: inline-block;
	}
	
	.content{
		margin-top: 15rpx;
		height: auto;
		word-wrap: break-word;
	}
	
	.Interaction{
		margin-top: 10rpx;
		column-count:3;
		column-gap:60rpx;
	}
	.InteractionNum{
		color: #8a8a8a;
		display: inline-block;
		vertical-align: 15rpx;
		margin-left: 5rpx;
	}
	.Interaction image{
		width: 50rpx;
	}
</style>