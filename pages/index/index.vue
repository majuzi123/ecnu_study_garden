<template>
	<view class="home">
		<view class="homeHeader">
			<view class="homeHeaderItem" :class="headerIndex===0?'homeHeaderItemActive':''" @tap="changeHeaderNav(0)">{{headerContent[0].name}}</view>
			<view class="homeHeaderItem" :class="headerIndex===1?'homeHeaderItemActive':''" @tap="changeHeaderNav(1)">{{headerContent[1].name}}</view>
		</view>
		<swiper @change="onChangeIndex" class="homeBody" :current="headerIndex" :style="'height:'+contentHeight+'px;'">
			<swiper-item>
				<view class="homeData1">
					<IndexDiscover></IndexDiscover>
				</view>
			</swiper-item>
			<swiper-item>
				<view class="homeData2">
					<IndexConcern></IndexConcern>
				</view>
			</swiper-item>
		</swiper>
		
	</view>
</template>

<script>
	import IndexDiscover from '../../components/IndexDiscover/IndexDiscover'
	import IndexConcern from '../../components/IndexConcern/IndexConcern.vue'
	export default {
		name:'Index',
		data() {
			return {
				headerIndex:0,
				headerContent:[
					{'name':'发现'},
					{'name':'关注'}
				],
				// 内容块的高度
				contentHeight:0
			}
		},
		methods:{
			changeHeaderNav(val){
				this.headerIndex=val
			},
			onChangeIndex(e){
				this.changeHeaderNav(e.detail.current)
			}
		},
		components:{
			IndexDiscover,
			IndexConcern,
		},
		onReady(){
			//搞定swipper高度设置
			let view1 = uni.createSelectorQuery().select(".homeData1");
			let view2 = uni.createSelectorQuery().select(".homeData2");
			view1.fields({
			  size: true,
			  scrollOffset: false
			}, data => {
				if(this.contentHeight<data.height) this.contentHeight=data.height;
			}).exec();
			view2.boundingClientRect(data => {
				if(this.contentHeight<data.height) this.contentHeight=data.height;
			}).exec()
		},
	}
</script>

<style scoped>
	/* 首页头部导航栏 */
	.homeHeader{
		background-color: white;
		height: 100rpx;
		width: 100%;
		text-align: center;
		position: fixed;
		top: var(--window-top);
		left: 0;
		z-index: 10;
	}
	.homeHeaderItem{
		display: inline-block;
		font-size: 40rpx;
		line-height: 100rpx;
		padding:0 30rpx;
	}
	.homeHeaderItemActive{
		border-bottom: 2px solid #ffcc00;
		color: #ffcc00;
	}
	/* 中部组件部分 */
	.homeBody{
		margin-top: 110rpx;
	}
</style>
