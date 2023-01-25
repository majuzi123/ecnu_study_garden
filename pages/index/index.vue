<template>
	<view class="home">
		<view class="homeHeader">
			<view class="homeHeaderItem" :class="headerIndex===0?'homeHeaderItemActive':''" @tap="changeHeaderNav(0)">{{headerContent[0].name}}</view>
			<view class="homeHeaderItem" :class="headerIndex===1?'homeHeaderItemActive':''" @tap="changeHeaderNav(1)">{{headerContent[1].name}}</view>
		</view>
		<swiper @change="onChangeIndex" class="homeBody" :current="headerIndex">
			<swiper-item>
				<IndexDiscover></IndexDiscover>
			</swiper-item>
			<swiper-item>
				关注
			</swiper-item>
		</swiper>
		
	</view>
</template>

<script>
	import IndexDiscover from '../../components/IndexDiscover/IndexDiscover'
	export default {
		name:'Index',
		data() {
			return {
				headerIndex:0,
				headerContent:[
					{'name':'发现'},
					{'name':'关注'}
				]
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
			IndexDiscover
		}
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
		height: 2000rpx;
		margin-top: 110rpx;
	}
</style>
