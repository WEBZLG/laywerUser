<template>
	<view class="uni-list">
		<view class="uni-list-item disFlex" v-for="item in navlist" :key="item.id">
			<view class="itemText">{{ item.name }}</view>
			<view class="iconfont iconarrow-r"></view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			navlist: [
				{ id: 1, name: '婚姻家庭' },
				{ id: 2, name: '劳动用工' },
				{ id: 3, name: '合同纠纷' },
				{ id: 4, name: '交通事故' },
				{ id: 5, name: '房产纠纷' },
				{ id: 6, name: '债权债务' }
			]
		};
	}
};
</script>

<style lang="scss">
.uni-list {
	background-color: #ffffff;
	margin-top: 30rpx;
	.uni-list-item {
		padding: 40rpx 0;
		margin: 0 30rpx;
		font-size: 28rpx;
		font-weight: bold;
		border-bottom: 1px solid #e1e1e1;
		.itemText {
			color: #2e82ff;
		}
	}
}
</style>
