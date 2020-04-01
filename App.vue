<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
		
	}
</script>

<style lang="scss">
	/*每个页面公共css */
	image {
		display: block;
		height: 100%;
		width: 100%;
	}
	body{
		font-size: 28rpx;
		background-color: #F8F8F8;
	}
	.content {
		margin: 30rpx;
	}
	.flex{
		display: flex;
		align-items: center !important;
		flex-direction: row !important;
	}
	.disFlex{
		display: flex;
		flex-direction: row !important;
		justify-content: space-between !important;
	}
	.block{
		display: block !important;
	}
	.minImg{
		height: 168rpx;
		width: 168rpx;
		border-radius: 20rpx;
		margin-right: 30rpx;
	}
	.pubTitle{
		font-size: 32rpx;
		font-weight: bold;
	}
	.addrTitle{
		font-size: 24rpx;
		margin: 4rpx 0;
	}
	.tag{
		width: 118rpx;
		height: 30rpx;
		line-height: 30rpx;
		border-radius: 30rpx;
		text-align: center;
		color: #2E82FF;
		font-size: 20rpx;
		margin: 0 4rpx 4rpx 0;
		border: 1px solid #2E82FF !important;
	}
	.minInfo{
		flex: 1!important;
	}
	.articlImg{
		height: 224rpx;
		width: 224rpx;
		border-radius: 20rpx;
	}
	.laywerMark,
	.userMark{
		font-size: 22rpx;
		color: #ffffff;
		border-radius: 5rpx;
		width: 56rpx;
		height: 28rpx;
		line-height: 28rpx;
		text-align: center;
		margin: 0 20rpx;
	}
	.laywerMark{
		background-color:#FB8322 ;
	}
	.userMark{
		background-color: #2E82FF;
	}
	.minHead{
		height: 50rpx;
		width: 50rpx;
		border-radius: 50%;
		overflow: hidden;
	}
	.userinfo{
		padding: 40rpx 0;
	}
	.iconzuihuo{
		color: #FBA222;
		}
</style>
