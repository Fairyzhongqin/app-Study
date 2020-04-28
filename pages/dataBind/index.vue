<template>
	<view>
	<view>没关系 下一个会更好</view>
	<view>{{msg}}</view>
	<view>{{flag ? '青青子衿' : "悠悠我心"}}</view>
	<view v-for="(item,index) in list" :key="item.id">
		序号：{{index}},姓名:{{item.name}},年龄:{{item.age}}
	</view>
	<button size="mini" type="primary" @click="handle($event)">我是正义的按钮</button>
	</view>
</template>

<script>
	export default {
		data() {
			return{
				msg:'自己要更好 才能遇到更好的人',
				flag:true,
				list:[{
					id:0,
					name:'张一元',
					age:20
				},{
					id:1,
					name:'李媛媛',
					age:30
				},{
					id:2,
					name:'江文道',
					age:40
				}]
			}
		},
			
		methods:{
			handle(e) {
				console.log(e)
				alert('多点甜')
			}
		},
		onLoad:function() {
			console.log('监听页面加载')
		},
		onShow:function(){
			console.log('监听页面显示')
		},
		onHide:function(){
			console.log('监听页面隐藏')
		}
	}
</script>

<style>
</style>
