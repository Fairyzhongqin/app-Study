<template>
	<view>
		<view>这是联系我们页面</view>
		<view>
			<text selectable>这是text组件</text>
		</view>
		<view class="two" hover-class="hover-two">
		<view class="one" hover-class="hover-one" hover-stop-propagation :hover-start-time="1000"	:hover-stay-time="10000">有Hover样式</view>
		</view>
		<button size="mini" type="primary" plain loading>未来会更好</button>
		<image src="http://5b0988e595225.cdn.sohucs.com/images/20200426/82127d60738a45f6a87dc44eccf7b951.jpeg" ></image>
		<image src="http://5b0988e595225.cdn.sohucs.com/images/20200426/82127d60738a45f6a87dc44eccf7b951.jpeg" mode="scaleToFill"></image>
		<image src="http://5b0988e595225.cdn.sohucs.com/images/20200426/82127d60738a45f6a87dc44eccf7b951.jpeg" mode="aspectFit"></image>
		<image src="http://5b0988e595225.cdn.sohucs.com/images/20200426/82127d60738a45f6a87dc44eccf7b951.jpeg" mode="aspectFill"></image>
		<image src="http://5b0988e595225.cdn.sohucs.com/images/20200426/82127d60738a45f6a87dc44eccf7b951.jpeg" mode="widthFix"></image>
		<image src="http://5b0988e595225.cdn.sohucs.com/images/20200426/82127d60738a45f6a87dc44eccf7b951.jpeg" mode="heightFix"></image>
		<image src="http://5b0988e595225.cdn.sohucs.com/images/20200426/82127d60738a45f6a87dc44eccf7b951.jpeg" mode="top"></image>
		<view class="iconfont icon-duijizhexian"></view>
		<view class="iconfont icon-jinzitatu"></view>
		<svg class="icon" aria-hidden="true">
		    <use xlink:href="icon-duijizhexian"></use>
		</svg>
		<view class="father">
			<view class="son">独爱莲之出淤泥而不染</view>
		</view>
	</view>
	
</template>

<script>
</script>

<style lang="scss">
	.father {
		.son {
			color:blue;
			font-size: 40rpx;
		}
		}
	.one {
		width: 100px;
		height: 100px;
		border:1px solid red;
	}
	.hover-one {
		background-color: red;
	}
	.two {
		width: 200px;
		height: 200px;
		border: 1px solid green;
	}
	.hover-two {
		background-color: yellow;
	}
</style>
