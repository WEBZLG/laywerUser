<template>
	<view class="content">
		<view class="bg">
			<image src="../../static/denglu_bg.png"></image>
			<view class="title">
				<view class="logo"><image src="../../static/logo1.png" mode=""></image></view>
				<view class="">慕法法律咨询</view>
			</view>
		</view>
		<view class="iptBox">
			<view class="phone"><input type="text" class="ipt" value="" placeholder="请输入手机号" /></view>
			<view class="code">
				<input type="text" class="ipt" value="" placeholder="请输入验证码" />
				<button :class="{ active: !disableCodeBtn }" :disabled="disableCodeBtn" @tap="sendCode">{{ codeBtn.text }}</button>
			</view>
			<button type="primary" class="login">登录</button>
		</view>
		<view class="other disflex">
			<view class="line"></view>
			<view class="second">第三方登录</view>
			<view class="line"></view>
		</view>
		<view class="wechat">
			<image src="../../static/wechat.png" mode=""></image>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			seconds: 30,
			codeBtn: {
				text: '获取验证码',
				waitingCode: false,
				count: this.seconds
			}
		};
	},
	onLoad() {},
	methods: {
		sendCode: function() {
			this.codeBtn.waitingCode = true;
			this.codeBtn.count = this.seconds;
			this.codeBtn.text = this.codeBtn.count + 's';

			let countdown = setInterval(() => {
				this.codeBtn.count--;
				this.codeBtn.text = this.codeBtn.count + 's';
				if (this.codeBtn.count < 0) {
					clearInterval(countdown);
					this.codeBtn.text = '重新发送';
					this.codeBtn.waitingCode = false;
				}
			}, 1000);
		}
	},
	computed: {
		disableCodeBtn: function() {
			return this.codeBtn.waitingCode;
		}
	}
};
</script>

<style lang="scss">
$color-primary: #2e82ff;
button[type='primary'] {
	background-color: $color-primary;
	font-size: 28rpx;
}
.code {
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	align-items: center;
	button {
		margin: 0;
		text-align: center;
		font-size: 28rpx !important;
		&:after {
			border: none;
		}
		&.active {
			background-color: $color-primary;
			color: $uni-text-color-inverse;
		}
	}
}
.bg {
	height: 440rpx;
	position: relative;
}

.title {
	position: absolute;
	top: 56rpx;
	left: 0;
	right: 0;
	text-align: center;
	color: #ffffff;
}

.logo {
	height: 96rpx;
	width: 96rpx;
	margin: 0 auto 20rpx;
}

.iptBox {
	margin: 0 30rpx;
}

.iptBox {
	.phone,
	.code {
		font-size: 28rpx;
		padding: 30rpx 0;
		border-bottom: 1px solid #e1e1e1;
	}
}
.login{
	border-radius: 35rpx;
	margin-top: 128rpx;
}
.other{
	margin: 110rpx 30rpx 50rpx;
}
.line{
	flex: 1;
	border-bottom: 1px solid #999999;
}
.second{
	color: #999999;
	margin: 0 10px;
}
.wechat{
	height: 64rpx;
	width: 64rpx;
	margin: 0 auto;
}
</style>
