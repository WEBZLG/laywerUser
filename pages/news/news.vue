<template>
	<view class="">
		<view class="">
			<view class="flex nav">
				<view class="flex">
					<view class="iconfont iconshouye-copy"></view>
					回到首页
				</view>
				<view class="rowLine"></view>
				<view class="flex">
					<view class="iconfont iconbianzu"></view>
					发布话题
				</view>
				<view class="rowLine"></view>
				<view class="flex">
					<view class="iconfont iconsousuo-copy"></view>
					搜索
				</view>
				<view class="rowLine"></view>
				<view class="flex">
					<view class="iconfont iconmy-selection"></view>
					我的话题
				</view>
			</view>
			<wuc-tab :tab-list="tabList" :tabCur.sync="TabCur" @change="tabChange"></wuc-tab>
		</view>
		<view class="content">
			<swiper :current="TabCur" duration="300" @change="swiperChange">
				<swiper-item v-for="(item, index) in tabList" :key="index">
					<mescroll-body ref="mescrollRef" @init="mescrollInit" @down="downCallback" @up="upCallback" :down="downOption" :up="upOption">
						<view class="msgItem">
							<view class="block">
								<text class="talk">#话题#</text>
								<text>所谓的“忠诚协议”到底签还是不签？要怎么签才好？法院判决告诉你答案！</text>
							</view>
							<view class="disFlex imgBox">
								<view class="articlImg"><image src="../../static/touxiang.png" mode=""></image></view>
								<view class="articlImg"><image src="../../static/touxiang.png" mode=""></image></view>
								<view class="articlImg"><image src="../../static/touxiang.png" mode=""></image></view>
							</view>
							<view class="disFlex userinfo">
								<view class="flex">
									<view class="minHead"><image src="../../static/touxiang.png" mode=""></image></view>
									<!-- <view class="userMark">用户</view> -->
									<view class="laywerMark">律师</view>
									<view class="userName">刘大大大大大彪</view>
								</view>
								<view class="flex">
									<view class="iconfont iconzuihuo"></view>
									<view class="hotNum">88888</view>
								</view>
							</view>
						</view>
						<view class="msgItem">
							<view class="block">
								<text class="talk">#话题#</text>
								<text>所谓的“忠诚协议”到底签还是不签？要怎么签才好？法院判决告诉你答案！</text>
							</view>
							<view class="disFlex imgBox">
								<view class="articlImg"><image src="../../static/touxiang.png" mode=""></image></view>
								<view class="articlImg"><image src="../../static/touxiang.png" mode=""></image></view>
								<view class="articlImg"><image src="../../static/touxiang.png" mode=""></image></view>
							</view>
							<view class="disFlex userinfo">
								<view class="flex">
									<view class="minHead"><image src="../../static/touxiang.png" mode=""></image></view>
									<!-- <view class="userMark">用户</view> -->
									<view class="laywerMark">律师</view>
									<view class="userName">刘大大大大大彪</view>
								</view>
								<view class="flex">
									<view class="iconfont iconzuihuo"></view>
									<view class="hotNum">88888</view>
								</view>
							</view>
						</view>
						<view class="msgItem">
							<view class="block">
								<text class="talk">#话题#</text>
								<text>所谓的“忠诚协议”到底签还是不签？要怎么签才好？法院判决告诉你答案！</text>
							</view>
							<view class="disFlex imgBox">
								<view class="articlImg"><image src="../../static/touxiang.png" mode=""></image></view>
								<view class="articlImg"><image src="../../static/touxiang.png" mode=""></image></view>
								<view class="articlImg"><image src="../../static/touxiang.png" mode=""></image></view>
							</view>
							<view class="disFlex userinfo">
								<view class="flex">
									<view class="minHead"><image src="../../static/touxiang.png" mode=""></image></view>
									<!-- <view class="userMark">用户</view> -->
									<view class="laywerMark">律师</view>
									<view class="userName">刘大大大大大彪</view>
								</view>
								<view class="flex">
									<view class="iconfont iconzuihuo"></view>
									<view class="hotNum">88888</view>
								</view>
							</view>
						</view>
					</mescroll-body>
				</swiper-item>
			</swiper>
		</view>
	</view>
</template>

<script>
import WucTab from '@/components/wuc-tab/wuc-tab.vue';
import MescrollMixin from '@/components/mescroll-uni/mescroll-mixins.js';
export default {
	mixins: [MescrollMixin], // 使用mixin
	data() {
		return {
			TabCur: 0,
			tabList: [{ name: '精选' }, { name: '订阅' }, { name: '精选' }, { name: '订阅' }, { name: '精选' }, { name: '订阅' }, { name: '精选' }, { name: '订阅' }],
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
			},
			// 列表数据
			dataList: []
		};
	},
	components: { WucTab },
	onLoad() {},
	methods: {
		// 横向选项卡
		tabChange(index) {
			this.TabCur = index;
		},
		swiperChange(e) {
			let { current } = e.target;
			this.TabCur = current;
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
	},
	computed: {}
};
</script>

<style lang="scss">
$color-orange: #fba222;
$color-primary: #2e82ff;
$color-white: #ffffff;

.flex {
	justify-content: space-evenly;
}
.rowLine {
	border: 1px dashed #dcdcdc;
	height: 28rpx;
}
.nav {
	font-weight: bold;
	line-height: 100rpx;
	color: $color-primary;
	margin: 30rpx 0;
	height: 100rpx;
	background-color: $color-white;
	border-bottom: 1px solid #e1e1e1;
}
.wuc-tab {
	top: -30rpx;
	background-color: $color-white;
}
.content {
	position: fixed;
	top: 160px;
	left: 0;
	right: 0;
	bottom: 50px;
}
uni-swiper {
	height: 100%;
}
.iconbianzu {
	font-size: 24rpx;
	margin-right: 4rpx;
}
.talk {
	color: $color-primary;
}
.block {
	font-weight: bold;
}
.imgBox {
	margin-top: 30rpx;
}
.msgItem {
	margin-bottom: 40rpx;
	border-bottom: 1px solid #e1e1e1;
}
swiper-item {
	overflow: auto;
}
</style>
