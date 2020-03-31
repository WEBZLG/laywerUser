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
		flex-direction: row !important;
	}
	.disFlex{
		display: flex;
		flex-direction: row !important;
		justify-content: space-between !important;
	}
</style>
