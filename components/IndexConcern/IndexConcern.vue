<template>
	<view>
		<!-- 关注列表 -->
		<view class="IndexConcernListContainer">
			<view class="IndexConcernListTitle">关注列表</view>
			<view class="IndexConcernListBody">
				<view class="IndexConcernListItem" v-for="(item,index) in concernList" :key="index">
					<image :src="item.img" alt="头像" mode="widthFix">
					<view class="IndexConcernListItemTitle">{{item.name}}</view>
				</view>
				<view class="IndexConcernListMore">></view>
			</view>
		</view>
		<!-- 每一个推荐作品 -->
		<view class="">
			<view v-for="(recommendItem,index) in recommendList" :key="index" class="recommendOpus">
				<IndexConcernRecommend :recommendItem="recommendItem"></IndexConcernRecommend>
			</view>
		</view>
	</view>
</template>

<script>
	import IndexConcernRecommend from './IndexConcernRecommend.vue'
	export default {
		name:"IndexConcern",
		data() {
			return {
				concernList:[
					{
						img:'../../static/index/index_discover/user_example.png',
						name:'我是1号',
					},
					{
						img:'../../static/index/index_discover/user_example.png',
						name:'我是2号',
					},
					{
						img:'../../static/index/index_discover/user_example.png',
						name:'我是3号',
					},
					{
						img:'../../static/index/index_discover/user_example.png',
						name:'我是4号',
					},
					{
						img:'../../static/index/index_discover/user_example.png',
						name:'我是5号,很长很长很长很长很长很长很长很长',
					}
				],
				recommendList:[
					{
						userImg:'../../static/index/index_discover/user_example.png',
						name:'小墨',
						time:'2021-02-01',
						opusImg:'../../static/example.png',
						opusIntro:'1111111111111111111111111111111',
						InterNum:[20,30,40],//顺序为：点赞、评论、收藏
					},
					{
						userImg:'../../static/index/index_discover/user_example.png',
						name:'小李',
						time:'2021-02-01',
						opusImg:'../../static/example.png',
						opusIntro:'1111111111111111111111111111111',
						InterNum:[20,30,40],
					},
					{
						userImg:'../../static/index/index_discover/user_example.png',
						name:'小白',
						time:'2021-02-01',
						opusImg:'../../static/example.png',
						opusIntro:'1111111111111111111111111111111',
						InterNum:[20,30,40],
					},
				]
			};
		},
		components:{IndexConcernRecommend,}
	}
</script>

<style scoped>
	.IndexConcernListContainer{
		width: 720rpx;
		margin: 10rpx 15rpx;
		padding-bottom: 20rpx;
		border-bottom: 10rpx lightgray solid;
	}
	.IndexConcernListTitle{
		font-size: 40rpx;
	}
	.IndexConcernListBody{
		width: 100%;
		text-align: center;
		margin-top: 10rpx;
	}
	.IndexConcernListItem image{
		width: 100rpx;
	}
	.IndexConcernListItem{
		display: inline-block;
		padding: 0rpx 15rpx;
	}
	.IndexConcernListItemTitle{
		width: 100rpx;
		line-height: 40rpx;
		overflow: hidden;
		white-space: nowrap;
	}
	.IndexConcernListMore{
		vertical-align:top;
		display: inline-block;
		line-height: 140rpx;
		height: 146rpx;
		width: 7%;
		margin-left: 15rpx;
		color: white;
		background-color: lightgray;
		border-radius: 20rpx;
	}
	.recommendOpus{
		padding-bottom: 10rpx;
		margin: 20rpx 15rpx;
		border-bottom: 10rpx solid lightgray;
	}
</style>