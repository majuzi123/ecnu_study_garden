<template>
	<view class="content">
		<view class="main">
			<lsj-upload ref="lsjUpload" width="100px" height="80rpx" childId="upload" :size="10" v-model="percent"
				@input="onInput" @callback="onCallback">
				<view class="btn" style="height: 80rpx;">选择附件上传</view>
			</lsj-upload>
		</view>
	</view>

</template>

<script>
	export default {
		data() {
			return {
				percent: '',
				userId: ''
			}
		},
		onReady() {
			// 初始化参数并创建上传DOM
			this.onCreate();
		},
		onLoad(options) {
			this.userId = options.userId
		},
		methods: {
			onCreate() {
				console.log('初始化附件插件');
				// 初始化参数并创建上传DOM
				this.$refs.lsjUpload.create({
					// #ifdef APP-PLUS
					cuWebview: this.$mp.page.$getAppWebview(), // app必传
					// #endif
					url: '', //替换为你的接口地址
					name: 'file', // 附件key
					size: 10, // 附件上传大小上限(M)，默认10M
					debug: true,
					//根据你接口需求自定义请求头
					header: {
						'Authorization': `token`
					},
					//根据你接口需求自定义body参数
					formData: {
						'orderId': 1000
					}
				});
			},
			onInput(e) {
				console.log('上传进度', e);
			},
			onCallback(e) {
				consoel.log('上传结果', e)
			},
		}
	}
</script>

<style>
	.content {
		width: 100%;
		height: 500px;
		position: relative;
	}

	.main {
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translateX(-50%);
	}

	.btn {
		height: 80rpx;
		background-color: #007AFF;
		color: #fff;
		border-radius: 10rpx;
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 28rpx;
	}
</style>
