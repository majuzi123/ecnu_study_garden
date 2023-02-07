<template>
	<view>
		<!-- <view class="list1-con-t">
			<view class="fu">
				<view class="fulist" v-for="(item,index) in fuList" :key="item.id" @click="fuBtn(item)">
					<view class="">
						{{item.originFileName}}
					</view>
					<view class="" @click.stop="delUserInfoAnnex(item)">
						<u-icon name="close-circle"></u-icon>
					</view>
				</view>
			</view> -->
		<!-- <view class="btn" @click="accessory">
			上传附件
		</view> -->
		<view class="com-item">
			<view class="com-wrap">
				<view class="cell">
					<navigator url="/pages/add_attachment/add_attachment" hover-class="none">
						<view class="cell-left">
							<view class="cell-text">
								附件上传区
							</view>
							<image class="arrow" src="/static/images/arrow_right.png" />
						</view>
						<!-- <view class="iconfont" /> -->
					</navigator>

				</view>
				<view class="cell">

					<view class="cell-left">
						<view class="cell-text">
							主题选择区
						</view>

						<image class="arrow" src="/static/images/arrow_right.png" />
					</view>
					<!-- <view class="iconfont" /> -->


				</view>
			</view>

		</view>

	</view>




</template>

<script>
	export default {
		name: "upload-file",
		data() {
			return {
				userId: '',
				fuList: [],
				array: ['中国', '美国', '巴西', '日本']
			}
		},
		onLoad(options) {
			this.userId = options.userId
		},
		methods: {
			bindPickerChange: function(e) {
				console.log('picker发送选择改变，携带值为', e.detail.value)
				this.index = e.detail.value
			},
			// 点击附件预览
			fuBtn(e) {
				console.log('点击附件', e);
				this.viewFile(e.filePath)
			},
			// 删除附件
			delUserInfoAnnex(e) {
				this.$api.delUserInfoAnnex(e.id).then(res => {
					console.log('删除', res);
					this.getAnnexList(e.userID)
				})

			},
			viewFile(e) {
				uni.downloadFile({
					url: this.baseUrl + e,
					success: function(res) {
						var filePath = res.tempFilePath;
						console.log(res);
						uni.openDocument({
							filePath: filePath,
							showMenu: true,
							success: function(res) {
								console.log('打开文档成功');
							}
						});
					}
				});
			}
		}
	}
</script>

<style>
	.com-item {
		padding-left: 20rpx;
		padding-right: 20rpx;
		margin-top: 20rpx;
		margin-bottom: 20rpx;
	}

	.com-item .com-wrap {
		border-radius: 25rpx;
		overflow: hidden;
	}

	.cell {
		height: 100rpx;
		padding-left: 20rpx;
		padding-right: 20rpx;
		margin-top: 0;
		display: flex;
		justify-content: space-between;
		align-items: center;
		background: #fff;
		border-bottom: 1px solid #f8f8f8;


	}

	.cell-left {
		display: flex;
		align-items: center;


	}

	.cell-icon {
		width: 50rpx;
		height: 50rpx;
		float: left;

	}

	.cell-text {
		width: 610rpx;
		color: #666;
		font-size: 28rpx;
		margin-left: 20rpx;
		color: #000;
	}

	.arrow {
		width: 30rpx;
		height: 30rpx;
	}

	.iconfont {
		font-size: 40rpx;
		color: #999;
	}
</style>
