<template>
	<view class="upload-box">
		<view>
			<image :src=cover @click="uploadImg" mode="aspectFill" />
		</view>
		<view class="text">
			<view class="title">
				<view class="name">
					<view style="white-space: nowrap;">作品：</view>
					<input class="uni-input" maxlength="10" placeholder="最大输入长度为10" />
				</view>

			</view>
			<view class="data">
				<text style="white-space: nowrap; font-size: 30rpx; color: black;">简介：</text>
				<textarea class="data-input"
					placeholder="最大输入长度为10snsnnsjncjnxjnjxcnjcnxjncjnjcncjncjcncjncjncjcnjcjncjncjcnj" />
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name: 'upload-box',
		data() {
			return {
				works: {
					'name': '发现',
					'intorduction': '可以很长很长很长很长很长很长很长很长很长很长很长很长很长很长很长很长很长很长'
				},
				cover: '/static/tabbar_icon/upload.png'
			}
		},
		methods: {
			uploadImg() {
				let that = this
				uni.chooseImage({
					success(res) {
						console.log(res.tempFilePaths)
						that.cover = res.tempFilePaths;
						console.log(that.cover)
					}
				})
			}
		}
	}
</script>

<style lang="scss">
	.upload-box {
		display: flex;
		font-family: sans-serif;
		margin-top: 50rpx;

		image {
			width: 150rpx;
			height: 150rpx;
			border-radius: 10px;
			margin-left: 30rpx;
			margin-top: 10rpx;
		}
	}

	.name {
		width: 500rpx;
		display: flex;
		//flex-wrap: nowrap;
		//justify-content: flex-start;
	}

	.text {
		margin-left: 30rpx;
		margin-top: 10rpx;
		/*display: flex;*/
		/*flex-direction: column;*/
		/*justify-content: space-between;*/
	}

	.title {
		font-size: 35rpx;
		color: #333;
		//margin-top: 20rpx;
		margin-bottom: 10rpx;
		/*text-overflow: -o-ellipsis-lastline;*/
		/*溢出内容隐藏*/
		overflow: hidden;
		/*文本溢出部分用省略号表示*/
		text-overflow: ellipsis;
		/*特别显示模式*/
		display: -webkit-box;
		/*行数*/
		-webkit-line-clamp: 2;
		line-clamp: 2;
		/*盒子中内容竖直排列*/
		-webkit-box-orient: horizontal;


	}

	.data {
		font-size: 20rpx;
		color: #999;
		//margin-bottom: 5rpx;
		display: flex;

	}

	.data-input {
		font-size: 25rpx;
		white-space: normal;
		overflow: auto;
		height: 150rpx;
	}
</style>
