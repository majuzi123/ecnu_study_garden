<template>
	<view>
		<upload-box></upload-box>
		<view class="text1">
			<textarea class="text-input"
				placeholder="最大输入长度为140snsnnsjncjnxjnjxcnjcnxjncjnjcncjncjcncjncjncjcnjcjncjncjcnj" />
		</view>
		<upload-file></upload-file>
		<view class="btn">
			<button class="button-yuanjiao" hover-class="bg-click">取消</button>
			<button class="button-yuanjiao" hover-class="bg-click">上传</button>
		</view>
	</view>
</template>

<script>
	export default {
		name: 'Upload',
		data() {
			return {

			}
		},
		methods: {

		}

	}
</script>

<style>
	/* .text1 {
		margin-left: 30rpx;
		margin-right: 30rpx;
		 border-radius: 5rpx; 
		border-style: solid;
		border-color: #c3c8ca;

	} */

	.text-input {
		margin-left: 30rpx;
		margin-right: 30rpx;
		/* border-radius: 5rpx; */
		border-style: solid;
		border-color: #c3c8ca;
		font-size: 30rpx;
		color: #000;
		white-space: normal;
		overflow: auto;
		height: 300rpx;
		width: 700rpx;
		background-color: #F7F8FA;
	}

	.button-yuanjiao {
		width: 300rpx;
		height: 100rpx;
		display: flex;
		margin-top: 50rpx;
		line-height: 50rpx;
		justify-content: center;
		border-radius: 10rpx;
		/* 这里可以改成渐变： background:linear-gradient(to right, #FFDE28,#FF3228) */
		background-color: #00aaff;
		font-size: 35rpx;

		padding-bottom: 0;
		padding-top: 15rpx;
	}

	.bg-click {
		background-color: #a7a9ff;
	}

	.btn {
		display: flex;
		margin-top: 100prx;
	}
</style>
