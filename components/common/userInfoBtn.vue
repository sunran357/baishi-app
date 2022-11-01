<template>
	<view class="user-info-container">
		<button class="user-info-btn" open-type="getUserInfo" @getuserinfo="mpGetUserInfo" withCredentials="true">
			<slot></slot>
		</button>
	</view>
</template>

<script>
	export default {
		name: 'userInfoBtn',
		data() {
			return {
				userInfo: {}
			}
		},
		methods: {
			mpGetUserInfo(result) {
			}
		}
	}
</script>

<style lang="less" scoped>
	.user-info-btn::after {
		border: 0;
	}

	.user-info-btn {
		background-color: transparent;
		line-height: 0;
		padding: 0;
		font-size: 0;
	}
</style>
