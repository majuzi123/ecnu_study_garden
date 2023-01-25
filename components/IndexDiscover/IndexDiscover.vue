<template>
	<view class="indexDiscover">
		<!-- 轮播图 -->
		<Banner></Banner>
		<!-- 子页面选项 -->
		<view class="indexBodyNav">
			<view class="indexBodyNavItem">
				<view class="NavItemImg"><img src="../../static/tabbar_icon/index.png"></view>
				<view>主题</view>
			</view>
			<view class="indexBodyNavItem">
				<view class="NavItemImg"><img src="../../static/tabbar_icon/index.png"></view>
				<view>论坛</view>
			</view>
			<view class="indexBodyNavItem">
				<view class="NavItemImg"><img src="../../static/tabbar_icon/index.png"></view>
				<view>排行榜</view>
			</view>
			<view class="indexBodyNavItem">
				<view class="NavItemImg"><img src="../../static/tabbar_icon/index.png"></view>
				<view>活动</view>
			</view>
		</view>
		<!-- 神仙作品展示 -->
		<!-- 神仙作品部分标题 -->
		<view class="indexDiscoverOpus">
			<view class="indexDiscoverOpusTitle"> 神仙作品</view>
			<Opus></Opus>
			<Opus></Opus>
		</view>
	</view>
</template>

<script>
	import Banner from "./Banner.vue"
	import Opus from "./Opus.vue"
	export default {
		name:"IndexDiscover",
		data() {
			return {
				
			};
		},
		components:{Banner,Opus}
	}
</script>

<style scoped>
	/* 整体样式 */
	.indexDiscover{
		
	}
	
	
	/* 子页面选项 */
	.indexBodyNav{
		width: 720rpx;
		height: 200rpx;
		margin: 15rpx;
		text-align: center;
	}
	.indexBodyNavItem{
		display:inline-block;
		margin: 10rpx 40rpx;
		font-size: 30rpx;
	}
	.NavItemImg{
		background-color: lightgray;
		width: 100rpx;
		height: 100rpx;
		border-radius: 50%;
		padding: 15rpx 0;
	}
	.NavItemImg img{
		width: 60rpx;
		height: 60rpx;
		margin: 5rpx 0;
	}
	
	/* 神仙作品 */
	.indexDiscoverOpus{
		margin-top: -30rpx;
		width: 100%;
		padding: 0 10rpx;
	}
	.indexDiscoverOpusTitle{
		margin-left: 15rpx;
		padding-left: 50rpx;
		line-height: 80rpx;
		font-size: 38rpx;
		border-left: 10rpx solid #ffcc00;
	}
</style>