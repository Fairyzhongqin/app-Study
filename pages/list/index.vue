<template>
	<view>
		<view v-for="(item,index) in list" :key="index" class="listone">
			{{item}}
		</view>
		<button @click="pullDown">下拉刷新</button>
		<button @click="sendRequest">发送请求</button>
		<button @click="setStorage">存储数据</button>
		<button @click="getStorage">得到数据</button>
		<button @click="removeStorage">移除数据</button>
		<button @click="clear">清除所有</button>
		<button @click="uploadImg">上传图片</button>
		<image  v-for="(item) in imgSrc":src="item"></image>
	</view>
</template>

<script>
	export default{
		data() {
			return {
				list:["纸质",'平平','佳人醉'],
				imgSrc:''
			}
		},
		methods:{
			pullDown() {
				uni.startPullDownRefresh() //开启下拉刷新
			},
			sendRequest(){
				uni.request({
					url:'http://www.baidu.com',
					success:function(res) {
						console.log(res)
					}
				})
			},
			setStorage() {
				// uni.setStorage({
				//     key: 'helloappId',
				//     data: '123',
				//     success: function () {
				//         console.log('success');
				//     }
				// });
				uni.setStorageSync('helloId', '1232323');
			},
			getStorage() {
				// uni.getStorage({
				//     key: 'helloId',
				//     success: function (res) {
				//         console.log(res.data);
				//     }
				// });
				  const value = uni.getStorageSync('helloId');
				    if (value) {
				        console.log(value);
				    }
			},
			removeStorage(){
				// uni.removeStorage({
				//     key: 'helloappId',
				//     success: function (res) {
				//         console.log('success');
				//     }
				// });
				    uni.removeStorageSync('helloId');
			},
			clear() {
				uni.clearStorage();
			},
			uploadImg(){
				uni.chooseImage({
				    count: 6, //默认9
				    sizeType: ['original', 'compressed'], //可以指定是原图还是压缩图，默认二者都有
				    sourceType: ['album','compressed'], //从相册选择
				    success: (res) =>{
				       // console.log(res)
					   this.imgSrc = res.tempFilePaths
				    }
				});
			}
		},
		//监听下拉刷新
		 onPullDownRefresh() {
		        this.list=['平平','佳人醉',"纸质"]
		        setTimeout(function () {
		            uni.stopPullDownRefresh();
		        }, 1000);
		    },
			// 监听页面隐藏
			onReachBottom(){
				console.log('页面到底了')
				// this.list = [...this.list,...['自傲和','没闪','无所谓']]
				console.log(this.list)
			}
	}
</script>

<style>
	.listone {
		height: 300px;
		line-height: 200px;
	}
</style>
