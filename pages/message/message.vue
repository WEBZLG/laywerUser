<template>
	<view class="container">
		<view class="flex">
			<view class="msgImg msgIcon"><view class="iconfont iconlababofang"></view></view>
			<view class="">
				<view class="name">系统通知</view>
				<view class="">暂无系统通知</view>
			</view>
		</view>
		<view class="msgList">
			<view class="flex">
				<view class="msgImg">
					<view class="dot">2</view>
					<image src="../../static/touxiang.png" mode=""></image>
				</view>
				<view class="msgName">
					<view class="name">王律师</view>
					<view class="overEllipsis">您好，您的诉讼我已经收到，请问您签合同的...</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {};
	},
	onLoad() {
		uni.setTabBarBadge({
			index: 2,
			text: '1'
		});
	},
	methods: {},
	computed: {}
};
</script>

<style lang="scss">
.container {
	background-color: #ffffff;
	position: relative;
	top: 30rpx;
	.flex {
		padding: 30rpx 0;
		margin: 0 30rpx;
		border-bottom: 1px solid #dcdcdc;
		.name {
			font-weight: bold;
			font-size: 28rpx;
		}
	}
	.msgImg {
		height: 118rpx;
		width: 118rpx;
		border-radius: 15rpx;
		overflow: hidden;
		margin-right: 30rpx;
		position: relative;
	}
	.msgIcon {
		background-color: #2e82ff;
		color: #ffffff;
		line-height: 118rpx;
		text-align: center;
		.iconlababofang {
			font-size: 48rpx;
		}
	}
	.msgList {
		position: fixed;
		top: 150rpx;
		left: 0;
		right: 0;
		bottom: 50rpx;
		overflow: auto;
		background-color: #ffffff;
	}
	.msgName{
		width: 76%;
	}
}
</style>
