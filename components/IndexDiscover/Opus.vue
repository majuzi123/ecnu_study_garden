<template>
	<view class="OpusWhole">
		<image :src="opus.img" alt="一张好看的图片" mode="widthFix">
		<view class="bigContainer">
			<view class="OpusTitle">{{opus.name}}</view>
			<view class="OpusInteractions">
				<!-- 点赞 -->
				<view class="OpusInteraction">
					<image src="../../static/index/index_discover/favour.png">
					<view class="OpusInteractionTitle">111w</view>
				</view>
				<!-- 评论 -->
				<view class="OpusInteraction">
					<image src="../../static/index/index_discover/commit.png">
					<view class="OpusInteractionTitle">111w</view>
				</view>
				<!-- 收藏 -->
				<view class="OpusInteraction">
					<image src="../../static/index/index_discover/collect.png">
					<view class="OpusInteractionTitle">111w</view>
				</view>
			</view>
		</view>
		<!-- 个人信息 -->
		<view class="OpusUser">
			<image src="../../static/index/index_discover/user_example.png">
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
		},
		props:['opus']
	}
</script>

<style scoped>
	/* 整体 */
	.OpusWhole{
		width: 345rpx;
		margin: 15rpx 10rpx;
		border-radius: 15rpx;
	}
	.OpusWhole image{
		width: 100%;
		border-radius: 15rpx;
	}
	.OpusTitle{
		line-height: 39rpx;
		text-overflow: -o-ellipsis-lastline;
		overflow: hidden;
		text-overflow: ellipsis;
		display: -webkit-box;
		-webkit-line-clamp: 2;
		line-clamp: 2;
		-webkit-box-orient: vertical;
		min-height: 39rpx;
		max-height: 78rpx;
	}
	.bigContainer{
		padding: 22rpx;
		font-size: 24rpx;
		padding-top:0rpx;
	}
	/* 点赞等互动部分 */
	.OpusInteractions{
		text-align: center;
	}
	.OpusInteraction{
		display: inline-block;
		margin: 10rpx 5rpx;
	}
	.OpusInteractions image{
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
	.OpusUser image{
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