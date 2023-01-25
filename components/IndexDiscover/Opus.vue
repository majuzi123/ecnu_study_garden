<template>
	<view class="OpusWhole">
		<img src="../../static/example.png" alt="一张好看的图片" mode="widthFix">
		<view class="OpusInteractions">
			<!-- 点赞 -->
			<view class="OpusInteraction">
				<img src="../../static/index/index_discover/favour.png">
				<view class="OpusInteractionTitle">111w</view>
			</view>
			<!-- 评论 -->
			<view class="OpusInteraction">
				<img src="../../static/index/index_discover/commit.png">
				<view class="OpusInteractionTitle">111w</view>
			</view>
			<!-- 收藏 -->
			<view class="OpusInteraction">
				<img src="../../static/index/index_discover/collect.png">
				<view class="OpusInteractionTitle">111w</view>
			</view>
		</view>
		
		<!-- 个人信息 -->
		<view class="OpusUser">
			<img src="../../static/index/index_discover/user_example.png">
			<view class="OpusUserName">小墨</view>
		</view>
	</view>
</template>

<script>
	export default{
		name:'Opus',
		data(){
			return {
				
			}
		}
	}
</script>

<style scoped>
	/* 整体 */
	.OpusWhole{
		width: 345rpx;
		margin: 15rpx 10rpx;
		display: inline-block;
		border-radius: 15rpx;
		border: 2rpx solid lightgray;
	}
	.OpusWhole img{
		width: 100%;
		border-radius: 15rpx;
	}
	/* 点赞等互动部分 */
	.OpusInteractions{
		text-align: center;
	}
	.OpusInteraction{
		display: inline-block;
		margin: 10rpx 5rpx;
	}
	.OpusInteractions img{
		width: 35rpx;
		height: 35rpx;
	}
	.OpusInteractionTitle{
		display: inline-block;
	}
	/* 头像和作者部分 */
	.OpusUser{
		margin: 20rpx 10rpx;
		height: 50rpx;
	}
	.OpusUser img{
		width:50rpx;
		height: 50rpx;
	}
	.OpusUserName{
		display: inline-block;
		vertical-align: top;
		margin-left: 15rpx;
		line-height: 50rpx;
	}
</style>