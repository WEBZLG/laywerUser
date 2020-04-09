<template>
	<view class="">
		<view class="myBg">
			<image src="../../static/my_bg.png" mode=""></image>
			<view class="myImg">
				<view class="circleBig">
					<view class="circleSmall"><image src="../../static/touxiang.png" mode=""></image></view>
				</view>
				<view class="loginBtn">请点击头像登录</view>
			</view>
		</view>
		<view class="myNav">
			<view class="disFlex">
				<view class="flex">
					<view class="iconfont icongerenxinxi1"></view>
					<view class="navText">个人信息</view>
				</view>
				<view class="iconfont iconarrow-r"></view>
			</view>
			<view class="disFlex">
				<view class="flex">
					<view class="iconfont icondingdan"></view>
					<view class="navText">我的订单</view>
				</view>
				<view class="iconfont iconarrow-r"></view>
			</view>
			<view class="disFlex">
				<view class="flex">
					<view class="iconfont iconshoucangchenggong"></view>
					<view class="navText">我的收藏</view>
				</view>
				<view class="iconfont iconarrow-r"></view>
			</view>
			<view class="disFlex">
				<view class="flex">
					<view class="iconfont iconhuati"></view>
					<view class="navText">我的话题</view>
				</view>
				<view class="iconfont iconarrow-r"></view>
			</view>
		</view>
		<view class="otherNav">
			<view class="disFlex">
				<view class="flex">
					<view class="iconfont iconguanyu"></view>
					<view class="navText">关于我们</view>
				</view>
				<view class="iconfont iconarrow-r"></view>
			</view>
			<view class="disFlex">
				<view class="flex">
					<view class="iconfont iconlianxi"></view>
					<view class="navText">联系我们</view>
				</view>
				<view class="iconfont iconarrow-r"></view>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {};
	},
	onLoad() {},
	methods: {},
	computed: {}
};
</script>

<style lang="scss">
.myBg {
	height: 320rpx;
	.myImg {
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		margin-left: 0;
	}
	.circleBig {
		width: 170rpx;
		height: 170rpx;
		border-radius: 50%;
		border: 7rpx solid #99c7fd;
		margin: 10rpx auto;
	}
	.circleSmall {
		height: 158rpx;
		width: 158rpx;
		border-radius: 50%;
		overflow: hidden;
		border: 7rpx solid #e8f5fe;
	}
	.loginBtn {
		text-align: center;
		font-size: 32rpx;
		color: #ffffff;
		margin-top: 20rpx;
	}
}
.disFlex {
	padding: 40rpx 0;
	margin: 0 30rpx;
	align-items: center;
	border-bottom: 1px solid #e1e1e1;
	.navText {
		font-size: 28rpx;
		font-weight: bold;
		margin-left: 20rpx;
	}
	.icongerenxinxi1 {
		color: #F6A201;
	}
	.icondingdan{
		color: #1AA84D;
	}
	.iconshoucangchenggong{
		color: #1AA84D;
	}
	.iconhuati{
		color: #948CFB;
	}
	.iconguanyu{
		color: #FF7290;
	}
	.iconlianxi{
		color: #008AFF;
	}
}
.myNav,
.otherNav {
	background-color: #ffffff;
}
.otherNav {
	margin-top: 30rpx;
}
</style>
