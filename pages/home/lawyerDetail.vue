<template>
	<view class="">
		<view class="topBg">
			<view class="myImg">
				<view class="circleBig">
					<view class="circleSmall"><image src="../../static/touxiang.png" mode=""></image></view>
				</view>
				<view class="name">王律师</view>
				<view class="name">王者律师事务所</view>
			</view>
			<view class="flex">
				<view class="">
					<view class="">123</view>
					<view class="">服务人次</view>
				</view>
				<view class="line"></view>
				<view class="">
					<view class="">100%</view>
					<view class="">好评率</view>
				</view>
			</view>
		</view>
		<view class="modelBg">
			<view class="headline">
				<view class="caption"><view>擅长领域</view></view>
			</view>
			<view class="flex tags">
				<view class="tag">婚姻家庭</view>
				<view class="tag">婚姻家庭</view>
				<view class="tag">婚姻家庭</view>
				<view class="tag">婚姻家庭</view>
				<view class="tag">婚姻家庭</view>
				<view class="tag">婚姻家庭</view>
				<view class="tag">婚姻家庭</view>
				<view class="tag">婚姻家庭</view>
			</view>
		</view>
		<view class="modelBg">
			<view class="headline">
				<view class="caption"><view>律师服务</view></view>
			</view>
			<view class="">
				<scroll-view class="scroll-view" scroll-x="true" scroll-left="120">
					<view class="scroll-view-item">A</view>
					<view class="scroll-view-item">A</view>
					<view class="scroll-view-item">A</view>
					<view class="scroll-view-item">A</view>
					<view class="scroll-view-item">A</view>
					<view class="scroll-view-item">A</view>
					<view class="scroll-view-item">A</view>
					<view class="scroll-view-item">A</view>
				</scroll-view>
			</view>
		</view>
	</view>
</template>

<script></script>

<style lang="scss">
$color-white: #ffffff;
$color-orange: #fba222;
$color-primary: #2e82ff;
.topBg {
	height: 438rpx;
	background: linear-gradient(180deg, rgba(38, 124, 251, 1), rgba(47, 172, 252, 1));
	.myImg {
		padding-top: 10rpx;
	}
	.circleBig {
		width: 170rpx;
		height: 170rpx;
		border-radius: 50%;
		border: 7rpx solid #99c7fd;
		margin: 0 auto;
	}
	.circleSmall {
		height: 158rpx;
		width: 158rpx;
		border-radius: 50%;
		overflow: hidden;
		border: 7rpx solid #e8f5fe;
	}
	.name {
		text-align: center;
		font-weight: bold;
		font-size: 32rpx;
		color: $color-white;
		line-height: 64rpx;
	}
	.flex {
		justify-content: space-around;
		text-align: center;
		color: $color-white;
	}
	.line {
		border-right: 1px dashed $color-white;
		height: 15px;
	}
}
.modelBg {
	margin: 30rpx 0;
	background-color: $color-white;
	.headline {
		border-bottom: 1px solid #e1e1e1;
		padding: 30rpx;
	}
	.caption {
		font-size: 32rpx;
		color: $color-primary;
		border-left: 8rpx solid $color-orange;
		padding-left: 10rpx;
		.swipLeft {
			color: #333333;
		}
	}
	.tags {
		flex-wrap: wrap;
		padding: 22rpx 14rpx;
		.tag {
			margin: 8rpx 10rpx;
		}
	}
	.scroll-view {
		white-space: nowrap;
		.scroll-view-item {
			height: 180rpx;
			width: 180rpx;
			display: inline-block;
		}
	}
}
</style>
