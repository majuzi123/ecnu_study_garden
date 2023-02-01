<template>
	<view class="recommend">
		<!-- 头像及上传信息 -->
		<view class="recommendHeader">
			<image src="../../static/index/index_discover/user_example.png" alt="头像">
			<view class="recommendUserInfo">
				<view>小墨</view>
				<view>2021-02-01</view>
			</view>
		</view>
		<!-- 关于作品 -->
		<view class="recommendBody">
			<view class="recommendOpusLeft">
				<image src="../../static/example.png" mode="aspectFit">
			</view>
			<view class="recommendOpusRight">
				<view class="recommendOpusIntro">1111111111111111111111111111111111111111111111111111111111111111111111111111111111111</view>
				<view class="recommendOpusInteractions">
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
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		name:'IndexConcernRecommend',
		data(){
			return {
				
			}
		},
		props:['recommendItem'],
	}
</script>

<style scoped>
	.recommendHeader image{
		width: 90rpx;
		height: 90rpx;
	}
	.recommendUserInfo{
		display: inline-block;
		vertical-align: top;
		padding-top: 10rpx;
		margin-left: 40rpx;
		line-height: 40rpx;
	}
	.recommendBody{
		width: 720rpx;
	}
	
	.recommendOpusLeft{
		float: left;
	}
	.recommendOpusLeft image{
		background-color: lightgray;
		border-radius: 15rpx;
		width:300rpx;
		height:225rpx;
	}
	.recommendOpusRight{
		height: 225rpx;
		margin-bottom: 10rpx;
		margin-left: 10rpx;
		display: inline-block;
		padding: 10rpx 0;
	}
	.recommendOpusIntro{
		width: 400rpx;
		height: 132rpx;
		line-height: 44rpx;
		overflow: hidden;
		word-break: break-all;
		text-overflow:ellipsis;
	}
	.OpusInteractions{
		text-align: center;
	}
	.OpusInteraction{
		display: inline-block;
		margin: 10rpx 25rpx;
	}
	.OpusInteractions image{
		width: 35rpx;
		height: 35rpx;
	}
</style>