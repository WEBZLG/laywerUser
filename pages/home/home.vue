<template>
	<view>
		<view class="uni-padding-wrap">
			<view class="page-section swiper">
				<view class="page-section-spacing">
					<swiper class="swiper" indicator-dots="true" autoplay="true" indicator-active-color="#FBA222" indicator-color="#ffffff" circular="true">
						<swiper-item><image src="../../static/banner1.jpg" mode=""></image></swiper-item>
						<swiper-item><image src="../../static/banner1.jpg" mode=""></image></swiper-item>
						<swiper-item><image src="../../static/banner1.jpg" mode=""></image></swiper-item>
					</swiper>
				</view>
			</view>
		</view>
		<view class="content">
			<view class="caption disFlex">
				<view>常用工具</view>
				<view class="swipLeft">左滑更多</view>
			</view>
			<view class="uni-padding-wrap swiperTool">
				<view class="page-section swiper">
					<view class="page-section-spacing">
						<swiper class="swiper" indicator-dots="true" indicator-active-color="#FBA222" indicator-color="#2e82ff">
							<swiper-item>
								<view class="toolList disFlex">
									<view class="toolItem">
										<view class="toolIcon"><image src="../../static/1.png" mode=""></image></view>
										<view>免费咨询</view>
									</view>
									<view class="toolItem">
										<view class="toolIcon"><image src="../../static/2.png" mode=""></image></view>
										<view>专业咨询</view>
									</view>
									<view class="toolItem">
										<view class="toolIcon"><image src="../../static/3.png" mode=""></image></view>
										<view>找律师</view>
									</view>
									<view class="toolItem">
										<view class="toolIcon"><image src="../../static/4.png" mode=""></image></view>
										<view>律师函件</view>
									</view>
									<view class="toolItem">
										<view class="toolIcon"><image src="../../static/5.png" mode=""></image></view>
										<view>合同审核</view>
									</view>
								</view>
							</swiper-item>
							<swiper-item>
								<view class="toolList disFlex">
									<view class="toolItem">
										<view class="toolIcon"><image src="../../static/6.png" mode=""></image></view>
										<view>司考在线</view>
									</view>
									<view class="toolItem">
										<view class="toolIcon"><image src="../../static/7.png" mode=""></image></view>
										<view>普法宣传</view>
									</view>
									<view class="toolItem">
										<view class="toolIcon"><image src="../../static/8.png" mode=""></image></view>
										<view>案例分析</view>
									</view>
									<view class="toolItem">
										<view class="toolIcon"><image src="../../static/9.png" mode=""></image></view>
										<view>法规法条</view>
									</view>
									<view class="toolItem">
										<view class="toolIcon"><image src="../../static/10.png" mode=""></image></view>
										<view>学科建设</view>
									</view>
								</view>
							</swiper-item>
						</swiper>
					</view>
				</view>
			</view>
			<view class="consult">
				<view class="caption disFlex">
					<view>热门咨询</view>
					<view class="swipLeft" @click="moreConsult">更多</view>
				</view>
				<view class="consultBox">
					<view class="consultList disFlex">
						<view class="consultItem"><image src="../../static/hunyin.png" mode=""></image></view>
						<view class="consultItem"><image src="../../static/laodong.png" mode=""></image></view>
					</view>
					<view class="consultList disFlex">
						<view class="consultItem"><image src="../../static/hetong.png" mode=""></image></view>
						<view class="consultItem"><image src="../../static/jiaotong.png" mode=""></image></view>
					</view>
					<view class="consultList disFlex">
						<view class="consultItem"><image src="../../static/fangchan.png" mode=""></image></view>
						<view class="consultItem"><image src="../../static/zhaiwu.png" mode=""></image></view>
					</view>
				</view>
			</view>
			<view class="laywerOffice">
				<view class="caption disFlex">
					<view>推荐事务所</view>
					<view class="swipLeft">更多</view>
				</view>
				<wuc-tab :tab-list="tabList" :tabCur.sync="TabCur" @change="tabChange"></wuc-tab>
				<swiper :current="TabCur" duration="300" @change="swiperChange">
					<swiper-item v-for="(item, index) in tabList" :key="index">
						<view class="flex msgItem">
							<view class="minImg">
								<image src="../../static/touxiang.png" mode=""></image>
							</view>
							<view class="minInfo">
								<view class="pubTitle">北京市XXX律师事务所</view>
								<view class="addrTitle">北京市</view>
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
						<view class="flex msgItem">
							<view class="minImg">
								<image src="../../static/touxiang.png" mode=""></image>
							</view>
							<view class="minInfo">
								<view class="pubTitle">北京市XXX律师事务所</view>
								<view class="addrTitle">北京市</view>
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
					</swiper-item>
				</swiper>
			</view>
			<view class="laywer">
				<view class="caption disFlex">
					<view>推荐律师</view>
					<view class="swipLeft" @click="moreLawyer">更多</view>
				</view>
				<wuc-tab :tab-list="tabList" :tabCur.sync="TabCur1" @change="tabChange1"></wuc-tab>
				<swiper :current="TabCur1" duration="300" @change="swiperChange1">
					<swiper-item v-for="(item, index) in tabList" :key="index">
						<view class="flex msgItem">
							<view class="minImg">
								<image src="../../static/touxiang.png" mode=""></image>
							</view>
							<view class="minInfo">
								<view class="pubTitle">王律师</view>
								<view class="addrTitle">北京市</view>
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
					</swiper-item>
				</swiper>
			</view>
		</view>
	</view>
</template>

<script>
import WucTab from '@/components/wuc-tab/wuc-tab.vue';
export default {
	data() {
		return {
			TabCur: 0,
			TabCur1: 0,
			tabList: [{ name: '精选' }, { name: '订阅' },{ name: '精选' }, { name: '订阅' },{ name: '精选' }, { name: '订阅' },{ name: '精选' }, { name: '订阅' }]
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
		tabChange1(index) {
			this.TabCur1 = index;
		},
		swiperChange1(e) {
			let { current } = e.target;
			this.TabCur1 = current;
		},
		// 搜索
		onNavigationBarButtonTap: function(e) {
			if (e.index == 0) {
				console.log('点击扫码按钮了');
			}
		},
		moreConsult(){
			uni.navigateTo({
				url: './moreConsult',
				success: res => {},
				fail: () => {},
				complete: () => {}
			});
		},
		moreLawyer(){
			uni.navigateTo({
				url: './moreLawyer',
				success: res => {},
				fail: () => {},
				complete: () => {}
			});
		}
	},
	computed: {}
}; 
</script>

<style lang="scss">
$color-orange: #fba222;
$color-primary: #2e82ff;
uni-swiper {
	height: 330rpx;
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
.swiperTool uni-swiper {
	height: 272rpx !important;
}
.toolList {
	text-align: center;
	margin-top: 50rpx;
	.toolIcon {
		height: 100rpx;
		width: 100rpx;
		margin-bottom: 20rpx;
	}
}
.consultList {
	display: flex;
	flex-direction: row;
	justify-content: space-between;
}
.flex .toolItem {
	margin-right: 36rpx;
}
.consultItem {
	width: 340rpx;
	height: 176rpx;
	margin-bottom: 10rpx;
}
.consultBox {
	margin: 50rpx 0;
}
.tags{
	flex-wrap: wrap;
}
.msgItem{
	align-content: center;
	margin-bottom: 30rpx;
}
.laywerOffice swiper,
.laywer swiper,
.laywer{
		margin-top: 30rpx;
}
.laywerOffice uni-swiper,
.laywer uni-swiper{
	height: 992rpx;
	}
</style>
