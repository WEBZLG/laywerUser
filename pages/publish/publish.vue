<template>
	<view class="content">
		<view class="caption">请选择服务类型</view>
		<view class="disFlex navItem">
			<view class="">
				<view class="type">免费咨询</view>
				<view class="">律师免费为您解答疑问</view>
			</view>
			<view class="iconfont iconarrow-r"></view>
		</view>
		<view class="disFlex navItem">
			<view class="">
				<view class="type">专业咨询 </view>
				<view class="">专业律师帮您“走出困扰”</view>
			</view>
			<view class="iconfont iconarrow-r"></view>
		</view>
		<view class="disFlex navItem">
			<view class="">
				<view class="type">律师函件</view>
				<view class="">催款、辟谣、声明、佐证的重要武器</view>
			</view>
			<view class="iconfont iconarrow-r"></view>
		</view>
		<view class="disFlex navItem">
			<view class="">
				<view class="type">合同审核</view>
				<view class="">优秀律师帮您规避合同“陷阱”</view>
			</view>
			<view class="iconfont iconarrow-r"></view>
		</view>
		<view class="disFlex navItem">
			<view class="">
				<view class="type">合同定制</view>
				<view class="">为您量身定制“专属合同”</view>
			</view>
			<view class="iconfont iconarrow-r"></view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
		}
	},
	onLoad() {},
	methods: {

	},
	computed: {

	}

};
</script>

<style lang="scss">
	.caption{
		font-size: 32rpx;
		color: #333333;
		font-weight: bold;
		text-align: center;
		}
	.navItem{
		align-items: center;
		background-color: #FFFFFF;
		padding: 30rpx;
		margin-top: 30rpx;
		line-height: 42rpx;
	}
	.type{
		font-size: 32rpx;
		color: #2E82FF;
	}
</style>
