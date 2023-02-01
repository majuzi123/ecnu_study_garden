<template>
	<view class="">
		<view class="container">
			<view class="navigator">
				<view class="navigatorItem">学习交流</view>
				<view class="navigatorItem">随笔感想</view>
				<view class="navigatorItem">考研升学</view>
				<view class="navigatorItem">水区灌溉</view>
			</view>
			<view class="content">
				<ForumItem></ForumItem>
			</view>
		</view>
		
	</view>
</template>

<script>
	import ForumItem from '../../components/Forum/ForumItem.vue'
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		},
		components:{ForumItem}
	}
</script>

<style scoped>
	.container{
		background-color: lightgray;
		display: flex;
		padding:10rpx 15rpx;
	}
	.navigator{
		position: fixed;
        top: 0;
        bottom: 0;
        left: 0;
        width: 200rpx;
        border-right: 1px solid #e4e6e9;
        background-color: #fff;
	}
	.navigatorItem{
		background-color: lightgray;
		color: white;
		width: 80%;
		text-align: center;
		line-height: 60rpx;
		border-radius: 50rpx;
		margin-left: 10%;
		margin-top: 50rpx;
		margin-bottom: 50rpx;
	}
	.content{
		position: fixed;
        top: 0;
        right: 0;
        bottom: 0;
        left: 200rpx;
        overflow-y: auto;
        background-color: lightgray;
	}
</style>
