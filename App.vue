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
		},
		onError:function(err) {
			console.log('App Error',err)
		}
	}
</script>
<!-- <script src="//at.alicdn.com/t/font_1787168_k5s7i93mbn.js"></script> -->
<!-- <script src="./static/fonts/iconfont.js"></script> -->
<style>
	/*每个页面公共css */
	/* (1)直接在线引用 */
	@import url('//at.alicdn.com/t/font_1787168_yx0u6lvb5jg.css');
	/* (2)引用本地 但是更新的需重新下载 */
	/* @import url("./static/fonts/iconfont.css"); */
	
	view {
		font-size: 88rpx;
		color:red;
	}
	   .icon {
	       width: 1em; height: 1em;
	       vertical-align: -0.15em;
	       fill: currentColor;
	       overflow: hidden;
	    }
</style>
