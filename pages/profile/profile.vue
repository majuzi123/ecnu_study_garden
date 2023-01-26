<template>
	<view class="container">
		<view class="content">

			<!-- 用户信息：昵称、权限、单位 -->
			<view class="fot-xh">

				<view class="pic">
					<image src="/static/images/LOGO.png" style="width: 100%; height: 100%; border-radius: 50%" />
				</view>
				<view class="txt">
					<view class="info">
						<view class="nickname">
							姓名
						</view>
						<view class="unit">
							<text>个人介绍</text>
						</view>
					</view>
				</view>

			</view>
		</view>

		<view class="title">作品列表</view>
		<view class="Index">
			<!-- 瀑布流布局列表 -->
			<view class="pubuBox">
				<view class="pubuItem">
					<view class="item-masonry" v-for="(item, index) in comList" :key="index">
						<image :src="item.img" mode="widthFix"></image>
						<view class="listtitle">
							<!-- 这是没有高度的父盒子（下半部分） -->
							<view class="listtitle1">{{ item.name }}</view>
							<!-- <view class="listtitle2">
								<text class="listtitle2son">￥</text>
								{{ item.commdityPrice }}
							</view> -->
							<view class="OpusInteractions">
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
							<view class="listtitle3">
								互动区
							</view>
						</view>
					</view>
				</view>
			</view>
		</view>



	</view>

</template>

<script>
	export default {
		data() {
			return {
				comList: [{
						img: "/static/images/LOGO.png",
						name: '名称，可以很长很长很长很长很长很长很长很长很长很长很长很长很长很长很长很长很长很长',

					}, {
						img: 'http://pic.sc.chinaz.com/Files/pic/pic9/202002/zzpic23327_s.jpg',
						name: '名称会在超出两行时候自动折叠',

					},
					{
						img: '/static/example.png',
						name: '只有一行标题时高度为39',

					}, {
						img: 'https://n.sinaimg.cn/sinakd20230125s/500/w800h500/20230125/d908-069c930d682ec4209cc2229cab516ee4.jpg',
						name: '具体样式您可以自定义',

					}, {
						img: 'https://nimg.ws.126.net/?url=http%3A%2F%2Fdingyue.ws.126.net%2F2023%2F0123%2Fbb3cc655j00roxt49002tc000hs00qog.jpg&thumbnail=660x2147483647&quality=80&type=jpg',
						name: 'vue的H5页面也是如此使用',

					},

				], //商品列表
			};
		},
		methods: {

		}
	}
</script>

<style>
	.container {
		display: flex;
		flex-direction: column;
	}

	.fot-xh .pic {
		float: left;
		height: 160rpx;
		width: 160rpx;
		margin-right: 50rpx;
		margin-left: 38rpx;
		margin-top: 60rpx;
	}

	.fot-xh .txt {
		padding: 15rpx 0;
		overflow: hidden;
		font-family: sans-serif;
	}

	.fot-xh .txt .info {
		margin-top: 80rpx;
		position: absolute;
		display: block;
	}

	.fot-xh .txt .info .nickname {
		height: 30rpx;
		width: 600rpx;
		font-size: 35rpx;
		margin-bottom: 26rpx;
		font-weight: bold;
	}

	.fot-xh .txt .info .right {
		height: 28rpx;
		width: 600rpx;
		font-size: 25rpx;
		margin-bottom: 13rpx;
	}

	.fot-xh .txt .info .unit {
		height: 28rpx;
		width: 600rpx;
		font-size: 25rpx;
		margin-bottom: 13rpx;
	}

	.masonry-header {
		margin: 0 calc(12 / 390 * 100vw);
		display: flex;
		justify-content: space-between;
		align-items: center;

	}

	.title {
		margin-top: 50rpx;
		margin-left: 50rpx;
		color: #353535;
		font-weight: bold;
		font-size: calc(18 / 390 * 100vw);
	}

	//瀑布流


	.pubuBox {
		padding: 22rpx;
	}

	.pubuItem {
		column-count: 2;
		column-gap: 20rpx;
	}

	.item-masonry {
		box-sizing: border-box;
		border-radius: 15rpx;
		overflow: hidden;
		background-color: #fff;
		break-inside: avoid;
		/*避免在元素内部插入分页符*/
		box-sizing: border-box;
		margin-bottom: 20rpx;
		box-shadow: 0px 0px 28rpx 1rpx rgba(78, 101, 153, 0.14);
	}

	.item-masonry image {
		width: 100%;
	}

	.listtitle {
		padding-left: 22rpx;
		font-size: 24rpx;
		padding-bottom: 22rpx;






	}

	.listtitle.listtitle1 {
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

	.listtitle.listtitle2 {
		color: #ff0000;
		font-size: 32rpx;
		line-height: 32rpx;
		font-weight: bold;
		padding-top: 22rpx;


	}

	.listtitle.listtitle2.listtitle2son {
		font-size: 32rpx;
	}

	.listtitle.listtitle3 {
		font-size: 28rpx;
		color: #909399;
		line-height: 32rpx;
		padding-top: 22rpx;
	}

	.Index {
		width: 100%;
		height: 100%;
		margin-top: 20rpx;
	}

	.OpusInteractions {
		text-align: center;
	}

	.OpusInteraction {
		display: inline-block;
		margin: 10rpx 5rpx;
	}

	.OpusInteractions img {
		width: 35rpx;
		height: 35rpx;
	}

	.OpusInteractionTitle {
		display: inline-block;
	}
</style>
