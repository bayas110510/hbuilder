<template>
	<view>
		<view class="title">
			<view >生命周期函数</view>
			<view >生命周期函数的概念：<text>一个对象从创建，运行，销毁的整个过程被称为生命周期</text></view>
			<view >生命周期函数：<text>在生命周期函数中的每个阶段伴随着每一个函数的触发，这些函数被称为生命周期函数</text></view>
		</view>
		<view class="cont">
			<view>应用的生命周期</view>
			<view v-for="(item,index) in List" :key="index">
				<view>{{item.name}}:<text>{{item.text}}</text></view>
			</view>
		</view>
		<!-- <view class="cont2">
			<view>页面的生命周期</view>
			<view v-for="(item,index) in List" :key="index">
				<view>{{item.name}}:<text>{{item.text}}</text></view>
			</view>
		</view> -->
	</view>
</template>

<script>
	export default {
		data() {
			return{
				List: [
					{
						name:'onLaunch',
						text: '当uni-app初始化完成时触发一次（全局只触发一次）'
					},
					{
						name:'onShow',
						text: '当uni-app启动，或从后台进入前台显示'
					},
					{
						name:'onHide',
						text: '当uni-app启动，从前台进入后台',
					},
					{
						name:'onError',
						text: '当uni-app 报错时触发'
					}
				]
			}
		},
		onLoad(){
			console.log('页面加载了')
		},
		onShow(){
			console.log('监听页面显示')
		},
		onReady(){
			console.log('监听页面初次渲染完成')
		},
		onHide(){
			console.log('监听页面隐藏')
		},
		onUnload(){
			console.log('监听页面卸载')
		}
	}
</script>
<style lang="scss">
	.title{
		padding: 20px;
		border-bottom: 1px solid #CCCCCC;
		view{
			font-size: 18px;
		}
		text{
			font-size: 14px;
			color: #666666;
		}
	}
	.cont{
		padding: 20px;
		border: 1px solid #333333;
		view{
			font-size: 18px;
			text{
				font-size: 14px;
				color:#666666; 
			}
		}
	}
</style>