<template>
	<view class="my-serch-container" :style="{'background-color': bgcolor}">
		<!-- 使用 uni-ui 提供的图标组件 -->
		<view class="my-serch-box" :style="{'border-radius' : radius + 'px'}" @click="onClick()">
			<uni-icons type="search" size="17"></uni-icons>
			<text class="placeholder">搜索</text>
		</view>
	</view>
</template>

<script>
	export default {
		props: {
			// 背景颜色
			bgcolor: {
				type: String,
				default: '#C00000'
			},
			// 圆角尺寸
			radius: {
				type: Number,
				default: 18
			}
		},
		data() {
			return {

			};
		},
		methods:{
			onClick() {
				this.$emit('click');
			}
		}

	}
</script>

<style lang="scss" scoped>
	.my-serch-container {
		height: 50px;
		// background-color: #C00000;
		display: flex;
		align-items: center;
		padding: 0 10px;

		.my-serch-box {
			height: 36px;
			background-color: #fff;
			// border-radius: 18px;
			width: 100%;
			display: flex;
			align-items: center;
			justify-content: center;

			.placeholder {
				font-size: 15px;
			}
		}
	}
</style>
