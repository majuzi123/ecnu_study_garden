<template>
	<view>
		<view class="activityContainer">
			<view class="activityName">{{actItem.name}}</view>
			<view class="activityContent">{{actItem.intro}}</view>
			<view class="activityFooter">
				<view class="activityNum">#{{actItem.peopleNum}}人已参加</view>
				<button>立即参与</button>
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		name:'ActivityItem',
		data(){
			return{
				
			}
		},
		props:['actItem'],
	}
</script>

<style scoped>
	.activityContainer{
		margin: 20rpx 20rpx;
		padding-bottom: -10rpx;
		border-radius: 20rpx;
		padding: 15rpx 15rpx;
		background-color: white;
	}
	.activityName{
		line-height: 40rpx;
		font-size: 35rpx;
		margin-bottom: 15rpx;
	}
	.activityContent{
		line-height: 35rpx;
		font-size: 28rpx;
	}
	.activityFooter{
		margin-top: 36rpx;
		width: 100%;
		height: 43rpx;
	}
	.activityNum{
		color: lightgray;
		float: left;
		vertical-align: middle;
	}
	.activityFooter button{
		margin-top: -24rpx;
		text-align: center;
		border-radius: 20rpx;
		height: 60rpx;
		font-size: 25rpx;
		margin-right: 20rpx;
		float: right;
		background-color: #ffcc00;
		color: white;
	}
</style>