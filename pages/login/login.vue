<template>
	<view>
		<view class="loginHeader">
			<image src="../../static/images/LOGO.png" mode="widthFix">
			<view class="loginHeaderText">欢迎来到狮学园！</view>
		</view>
		
		<form action="" class="loginForm">
			<view class="loginFormItem">
				<image src="../../static/images/login/userId.png" mode="widthFix"><input type="text" class="loginFormInput" placeholder="请输入用户名">
			</view>
			<view class="loginFormItem">
				<image src="../../static/images/login/password.png" mode="widthFix"><input type="password" class="loginFormInput" placeholder="请输入密码">
			</view>
			<button class="loginFormButton">登 录</button>
		</form>
	</view>
</template>

<script>
	export default {
		name:'login',
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	
	.loginHeader{
		text-align: center;
		padding-top: 140rpx;
		margin-bottom: -50rpx;
	}
	.loginHeader image{
		width: 400rpx;
	}
	.loginHeaderText{
		line-height: 100rpx;
		font-size: 40rpx;
	}
	.loginForm{
		text-align: center;
		padding: 100rpx 200rpx
	}
	.loginForm image{
		width: 80rpx;
	}
	.loginFormInput{
		display: inline-block;
		width: 300rpx;
	/* 	border: 2rpx solid lightgray; */
		border-radius: 15rpx;
		height: 75rpx;
		width: 400rpx;
		text-align: left;
		padding-left: 5rpx;
		font-size: 35rpx;
	}
	.loginFormItem{
		margin: 0rpx 130rpx;
		padding-bottom: 10rpx;
		padding-top: 80rpx;
		border-bottom: 2rpx solid black;
	}
	.loginFormButton{
		margin-top: 100rpx;
		width: 500rpx;
		border-radius: 50rpx;
		background-color: #ffcc00;
		color: white;
		font-size: 40rpx;
	}
</style>
