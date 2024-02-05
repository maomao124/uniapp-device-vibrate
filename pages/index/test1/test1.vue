<template>
	<view>
		<button type="primary" @click="button1" >振动</button>
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
			}
		}
	}
</script>

<style>
button{
	margin: 5px;
}
</style>
