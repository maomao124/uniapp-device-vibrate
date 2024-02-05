<template>
	<view>
		<button type="primary" @click="button1" >振动</button>
		<button type="primary" @click="button2" >振动 - 长</button>
		<button type="primary" @click="button3" >振动 - 短</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			button1()
			{
				uni.vibrate({
					success: () => {
						uni.showToast({
							title:'成功'
						})
					},
					fail: () => {
						uni.showToast({
							title:'失败'
						})
					}
				})
			},
			button2()
			{
				uni.vibrateLong({
					success: () => {
						uni.showToast({
							title:'成功'
						})
					},
					fail: () => {
						uni.showToast({
							title:'失败'
						})
					}
				})
			},
			button3()
			{
				uni.vibrateShort({
					success: () => {
						uni.showToast({
							title:'成功'
						})
					},
					fail: () => {
						uni.showToast({
							title:'失败'
						})
					}
				})
			}
		}
	}
</script>

<style>
button{
	margin: 5px;
}
</style>
