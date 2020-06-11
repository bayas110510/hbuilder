<template>
	<view>
		<view class="box">
			<button type="primary" size="mini" @click="chooseImg">上传图片</button>
			<view class="img-wrap">
				<image v-for="(item,index) in imgArr" :key= "index" :src="item" @click="previewImg(item)"></image>
			</view>
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				imgArr: []
			}
		},
		methods: {
			chooseImg(){
				uni.chooseImage({
					count:5,
					success: res=> {
						console.log(res)
						this.imgArr = res.tempFilePaths
						console.log(this.imgArr)
					}
				})
			},
			previewImg(current){
				console.log(current)
				uni.previewImage({
					current:current,
					urls:this.imgArr,
					loop:true,
					indicator: 'default'
				})
			}
		}
	}
</script>

<style lang="scss">
	.box{
		text-align: center;
	}
	.img-wrap{
		display: flex;
		flex-direction: row;
		flex-wrap: wrap; 
		image{
			width: 100px;
			height: 100px;
			margin: 5px;
		}
	}
</style>
