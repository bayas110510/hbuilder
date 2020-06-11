<template>
	<view>
		<view class="box">
			<view>数绑定的学习</view>
			<text>{{msg}}</text>
			<view>{{flag?'bayas':'tunnl'}}</view>
			<image :src="img" mode=""></image>
			<view v-for="(item,index) in arr" :key="item.id">
				{{item.name}}----{{item.age}}------{{item.gender}}
			</view>
			
		</view>
		<view>
			<view>绑定事件</view>
			<button type="primary" size="mini" @click="add(20,$event)">按钮</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				msg:'bayas&tunnl',
				flag:true,
				img:'../../static/wassim-chouak-oH6_OL_QvzU-unsplash.jpg',
				arr: [
					{
						name:'aaa',
						age: 23,
						gender: '男'
					},
					{
						name:'bbb',
						age: 20,
						gender: '女'
					},
					{
						name:'ccc',
						age: 26,
						gender: '男'
					},
					{
						name:'ddd',
						age: 18,
						gender: '女'
					}	
				]
			}
		},
		methods: {
			add(num,e){
				alert('点击事件已触发')
				console.log(num,e)
			}
		}
	}
</script>

<style>
	.box{
		border-bottom: 1px solid #333333;
		padding: 20px;
	}
</style>
