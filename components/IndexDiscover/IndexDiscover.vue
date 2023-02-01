<template>
	<view class="indexDiscover">
		<!-- 轮播图 -->
		<Banner></Banner>
		<!-- 子页面选项 -->
		<view class="indexBodyNav">
			<view class="indexBodyNavItem">
				<view class="NavItemImg"><image src="../../static/tabbar_icon/index.png"></view>
				<view>主题</view>
			</view>
			<view class="indexBodyNavItem">
				<view class="NavItemImg"><image src="../../static/tabbar_icon/index.png"></view>
				<view>论坛</view>
			</view>
			<view class="indexBodyNavItem">
				<view class="NavItemImg"><image src="../../static/tabbar_icon/index.png"></view>
				<view>排行榜</view>
			</view>
			<view class="indexBodyNavItem">
				<view class="NavItemImg"><image src="../../static/tabbar_icon/index.png"></view>
				<view>活动</view>
			</view>
		</view>
		<!-- 神仙作品展示 -->
		<!-- 神仙作品部分标题 -->
		<view class="indexDiscoverOpus">
			<view class="indexDiscoverOpusTitle"> 神仙作品</view>
			<view class="OpusContainer">
				<view v-for="(opus,index) in opusList" :key="index" class="Opuscontainer2">
						<Opus :opus="opus"></Opus>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import Banner from "./Banner.vue"
	import Opus from "./Opus.vue"
	export default {
		name:"IndexDiscover",
		data() {
			return {
				opusList:[
					{
						id:'000',
						img: "../../static/images/LOGO.png",
						name: '名称，可以很长很长很长很长很长很长很长很长很长很长很长很长很长很长很长很长很长很长',
					}, {
						id:'001',
						img: 'http://pic.sc.chinaz.com/Files/pic/pic9/202002/zzpic23327_s.jpg',
						name: '名称会在超出两行时候自动折叠',
					},
					{
						id:'002',
						img: '../../static/example.png',
						name: '只有一行标题时高度为39',
					}, {
						id:'003',
						img: 'https://n.sinaimg.cn/sinakd20230125s/500/w800h500/20230125/d908-069c930d682ec4209cc2229cab516ee4.jpg',
						name: '具体样式您可以自定义',
					}, {
						id:'004',
						img: 'https://nimg.ws.126.net/?url=http%3A%2F%2Fdingyue.ws.126.net%2F2023%2F0123%2Fbb3cc655j00roxt49002tc000hs00qog.jpg&thumbnail=660x2147483647&quality=80&type=jpg',
						name: 'vue的H5页面也是如此使用',
					},
				]
			};
		},
		components:{Banner,Opus}
	}
</script>

<style scoped>
	/* 整体样式 */
	.indexDiscover{
		
	}
	
	.OpusContainer{
		column-count: 2;
		column-gap: 10rpx;
		margin-top: 20rpx;
	}
	
	.Opuscontainer2{
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
	/* 子页面选项 */
	.indexBodyNav{
		width: 720rpx;
		height: 200rpx;
		margin: 15rpx;
		text-align: center;
	}
	.indexBodyNavItem{
		display:inline-block;
		margin: 10rpx 40rpx;
		font-size: 30rpx;
	}
	.NavItemImg{
		background-color: lightgray;
		width: 100rpx;
		height: 100rpx;
		border-radius: 50%;
		padding: 15rpx 0;
	}
	.NavItemImg image{
		width: 60rpx;
		height: 60rpx;
		margin: 5rpx 0;
	}
	
	/* 神仙作品 */
	.indexDiscoverOpus{
		margin-top: -30rpx;
		width: 100%;
		padding: 0 10rpx;
	}
	.indexDiscoverOpusTitle{
		margin-left: 15rpx;
		padding-left: 50rpx;
		line-height: 80rpx;
		font-size: 38rpx;
		border-left: 10rpx solid #ffcc00;
	}
</style>