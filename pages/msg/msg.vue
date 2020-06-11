<template>
	<view>
		<view class="text">
			<view>
				<text>text</text>
			</view>
			<view>
				<text>hello-bayastunnl</text>
			</view>
			
			<view>
				<text selectable>hello-bayas  tunnl</text>
			</view>
			<view>
				<text space="ensp">hello-bayas     tunnl</text>
			</view>
			<view>
				<text space="emsp">hello-bayas     tunnl</text>
			</view>
			<view>
				<text space="ebsp" style="font-size: 30px;">hello-bayas     tunnl</text>
			</view>
		</view>
		<view class="view">
			<view class="uni-padding-warp uni-common-mt">
				<view class="uni-title uni-common-mt">
					<view class="title">
						<view>view</view>
					</view>
					flex-direction: row
					<text>\n横向布局</text>
				</view>
				<view class="uni-flex uni-row">
					<view class="flex-item uni-bg-red">A</view>
					<view class="flex-item uni-bg-red">B</view>
					<view class="flex-item uni-bg-red">C</view>	
				</view>
				<view class="uni-title uni-common-mt">
					flex-direction: column
					<text>\n纵向布局</text>
				</view>
				<view class="uni-flex uni-column">
					<view class="flex-item uni-bg-red">A</view>
					<view class="flex-item uni-bg-red">B</view>
					<view class="flex-item uni-bg-red">C</view>	
				</view>
				<view class="uni-title uni-common-mt">
					float：left
					<text>\n浮动</text>
				</view>
				<view class="uni-flex uni-box">
					<view class="flex-item uni-bg-red">A</view>
					<view class="flex-item uni-bg-red">B</view>
					<view class="flex-item uni-bg-red">C</view>	
				</view>
				<view>
					<view class="boxOne" hover-class="box-active">box1</view> 
				</view>
			</view>
		</view>
		<view class="button-warp">
			<button type="primary" size="mini">按钮</button>
			<button type="primary" size="mini" plain>按钮</button>
		</view>
	</view>
</template>
<script>
</script>

<style>
	.text{
		border-bottom:1px solid #333333;
		padding: 20px;
	}
	.uni-padding-warp{
		padding: 20px;
		background-color: #e8e8e8;
		border-bottom: 1px solid #333333;
	}
	.button-warp{
		padding: 20px;
		background-color: #e8e8e8;
	}
	.title {
		text-align: center;
	}
	.title view{
		padding: 20px;
		border-bottom: 1px solid #CCCCCC;
		display: inline-block;
		font-weight: 400;
		color: #CCCCCC;
		box-sizing: border-box;
		height: 50px;
		/* line-height: 50px; */
	} 
	.uni-row{
		display: flex;
		flex-direction: row;
		padding: 10px;
		
	}
	.uni-title text {
		font-size: 12px;
		font-weight: 400;
		color: #CCCCCC;
	}
	.uni-row .flex-item{
		width: 100px;
		height: 100px;
	}
	.flex-item:first-child{
		background-color: red;
	}
	.flex-item:nth-child(2){
		background-color: #4CD964;
	}
	.flex-item:last-child{
		background-color: #007AFF;
	}
	.uni-column .flex-item{
		height: 100px;
	}
	.uni-column{
		display: flex;
		flex-direction: column;
		padding: 10px;
	}
	.uni-box{
		display: flex;
		flex-direction: row;
	}
	.uni-box .flex-item{
		width: 100px;
		height: 100px;
	}
	.boxOne{
		width: 100px;
		height: 100px;
		background-color: pink;
	}
	.box-active{
		background-color: #007AFF;
	}
</style>
