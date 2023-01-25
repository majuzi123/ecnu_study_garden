<template>
	<swiper class="indexDiscoverShow" autoplay interval="1500">
		<swiper-item><img src="../../static/logo.png" mode="heightFix"></swiper-item>
		<swiper-item><img src="../../static/example.png" mode="heightFix"></swiper-item>
	</swiper>
</template>

<script>
</script>

<style scoped>
	/* 轮播图 */
	.indexDiscoverShow{
		height: 350rpx;
		width: 700rpx;
		margin-left: 25rpx;
		background-color: lightgrey;
		text-align:center;
		border-radius: 20rpx;
	}
	.indexDiscoverShow img{
		height: 100%;
		width: auto;
		border-radius: 20rpx;
	}
</style>