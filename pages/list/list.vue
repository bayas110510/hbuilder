<template>
	<view>
		<button type="primary" @click="getData()">发送get请求</button>
		<button type="default" @click="setStorage()">存储数据</button>
		<button type="default" @click="getStorage()">获取数据</button>
		<button type="default" @click="removeStorage()">删除数据</button>
		
		<view>这是列表页 </view>
		<view class="box" v-for="(item,index) in list" :key="index">
			{{item}}
		</view>
		<!-- <button type="default" @click="pullDown()">下拉刷新</button> -->
	</view>
</template>

<script>
	export default{
		data() {
			return {
				list:['A','B','C','D','E','A','B','C','D','E']
			}
		},
		// 下拉刷新
		onPullDownRefresh() {
			console.log('触发了下拉')
			setTimeout(()=>{
				this.list=['前端','后端','大数据','全栈工程师','网页设计师','前端','后端','大数据','全栈工程师','网页设计师']
				// 关闭下拉
				uni.stopPullDownRefresh()
			},1000)
		},
		// 上拉刷新
		onReachBottom(){
			console.log('我也是有底线的')
			this.list = [...this.list,...['bayas']]
		},
		methods:{
			pullDown(){
				uni.startPullDownRefresh()
			},
			// 请求数据
			getData(){
				uni.request({
					url:'api/tunnl',
					success:(res)=> {
						console.log(res)
					}
				})
			},
			//上传数据
			setStorage(){
				uni.setStorage({
					key:'id',
					data:50,
					success() {
						console.log('存储成功 ')
					}
				})
			},
			// 获取数据
			getStorage() {
				uni.getStorage({
					key:"id",
					success(res) {
						console.log('获取成功',res)
					}
				})
			},
			// 删除数据 
			removeStorage(){
				uni.removeStorage({
					key:'id',
					success() {
						console.log('删除数据')
					}
				})
			}
			
		}
		
	}
</script>

<style>
	.box{
		height: 100px;
		line-height: 100px;
	}
	button{
		margin-bottom: 10px;
	}
</style>
