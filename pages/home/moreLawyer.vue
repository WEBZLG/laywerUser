<template>
	<view class="">
		<view class="topNav flex">
			<view class="uni-list">
				<view class="uni-list-cell flex">
					<view class="uni-list-cell-db">
						<picker @change="bindAddressChange" :value="indexAddress" :range="arrayAddress">
							<view class="uni-input">{{ address }}</view>
						</picker>
					</view>
					<view class="iconfont iconarrow-left"></view>
				</view>
			</view>
			<view class="uni-list">
				<view class="uni-list-cell flex">
					<view class="uni-list-cell-db">
						<picker @change="bindAreaChange" :value="indexArea" :range="arrayArea">
							<view class="uni-input">{{ area }}</view>
						</picker>
					</view>
					<view class="iconfont iconarrow-left"></view>
				</view>
			</view>
			<view class="uni-list">
				<view class="uni-list-cell flex">
					<view class="uni-list-cell-db">
						<picker @change="bindOrderChange" :value="indexOrder" :range="arrayOrder">
							<view class="uni-input">{{ order }}</view>
						</picker>
					</view>
					<view class="iconfont iconarrow-left"></view>
				</view>
			</view>
		</view>
		<view class="lawyerList">
			<mescroll-body ref="mescrollRef" @init="mescrollInit" @down="downCallback" @up="upCallback" :down="downOption" :up="upOption">
				<view class="flex msgItem" v-for="item in datalist" :key="this" @click="lawyerDetail">
					<view class="minImg"><image src="../../static/touxiang.png" mode=""></image></view>
					<view class="minInfo">
						<view class="pubTitle">北京市XXX律师事务所</view>
						<view class="addrTitle">北京市</view>
						<view class="addrTitle">北京市XXX律师事务所</view>
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
				</view>
			</mescroll-body>
		</view>
	</view>
</template>

<script>
import MescrollMixin from '@/components/mescroll-uni/mescroll-mixins.js';
export default {
	mixins: [MescrollMixin], // 使用mixin
	data() {
		return {
			datalist: [1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 11, 1],
			arrayAddress: ['中国', '美国', '巴西', '日本'],
			arrayArea: ['中国', '美国', '巴西', '日本'],
			arrayOrder: ['中国', '美国', '巴西', '日本'],
			indexAddress: 0,
			indexArea: 0,
			indexOrder: 0,
			address: '所在地区',
			area: '擅长领域',
			order: '智能排序',
			downOption: {
				use: true, // 是否启用下拉刷新; 默认true
				auto: false, // 是否在初始化完毕之后自动执行下拉刷新的回调; 默认true
				native: false // 启用系统自带的下拉组件,默认false;仅mescroll-body生效,mescroll-uni无效
				//(native: true, 则需在pages.json中配置"enablePullDownRefresh":true)
			},
			// 上拉加载的常用配置
			upOption: {
				use: true, // 是否启用上拉加载; 默认true
				auto: false, // 是否在初始化完毕之后自动执行上拉加载的回调; 默认true
				page: {
					num: 0, // 当前页码,默认0,回调之前会加1,即callback(page)会从1开始
					size: 10 // 每页数据的数量,默认10
				},
				noMoreSize: 5, // 配置列表的总数量要大于等于5条才显示'-- END --'的提示
				empty: {
					tip: '暂无相关数据'
				}
			}
		};
	},
	methods: {
		lawyerDetail(){
			uni.navigateTo({
				url: './lawyerDetail',
				success: res => {},
				fail: () => {},
				complete: () => {}
			});
		},
		bindAddressChange: function(e) {
			this.indexAddress = e.target.value;
			this.address = this.arrayAddress[e.target.value];
		},
		bindAreaChange: function(e) {
			this.indexArea = e.target.value;
			this.area = this.arrayArea[e.target.value];
		},
		bindOrderChange: function(e) {
			this.indexOrder = e.target.value;
			this.order = this.arrayOrder[e.target.value];
		},
		// 下拉加载
		downCallback() {
			console.log('xiala');
			this.mescroll.resetUpScroll();
		},
		/*上拉加载的回调*/
		upCallback(page) {
			console.log('shangla');
			let pageNum = page.num; // 页码, 默认从1开始
			let pageSize = page.size; // 页长, 默认每页10条
			// this.mescroll.endSuccess();
			// this.mescroll.endByPage();
			// this.$nextTick(() => {
			// });
			this.mescroll.endErr();
		}
	}
};
</script>

<style lang="scss">
.topNav {
	justify-content: space-around;
	background-color: #ffffff;
	padding: 35rpx;
	margin: 30rpx 0;
	.uni-input {
		margin-right: 18rpx;
		color: #2e82ff;
		font-weight: bold;
	}
}
.lawyerList {
	padding: 0 30rpx;
	position: fixed;
	top: 254rpx;
	left: 0;
	right: 0;
	bottom: 0;
	background-color: #ffffff;
	overflow: auto;
	.tags {
		flex-wrap: wrap;
	}
	.msgItem {
		align-content: center;
		margin: 30rpx 0;
	}
}
</style>
