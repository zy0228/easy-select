<template>
	<view class="content" @click="useOutClickSide">
		<view class="text-area">
			<text class="title">Deafult size</text>
		</view>
		<easy-select ref="easySelect" :value="selecValue" @selectOne="selectOne"></easy-select>
		<view class="text-area">
			<text class="title">Small size</text>
		</view>
		<easy-select ref="easySelect1" size="small" :value="selecValue1" @selectOne="selectOne1"></easy-select>
		<view class="text-area">
			<text class="title">Medium size</text>
		</view>
		<easy-select ref="easySelect2" size="medium" :value="selecValue2" @selectOne="selectOne2"></easy-select>
		<view class="text-area">
			<text class="title">Mini size</text>
		</view>
		<easy-select ref="easySelect3" size="mini" :value="selecValue3" @selectOne="selectOne3"></easy-select>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				selecValue: '双皮奶',
				selecValue1: '黄金糕',
				selecValue2: '蚵仔煎',
				selecValue3: '龙须面',
				selecValue4: '北京烤鸭'
			}
		},
		onLoad() {

		},
		methods: {
			selectOne(options) {
				this.selecValue = options.label
			},
			selectOne1(options) {
				this.selecValue1 = options.label
			},
			selectOne2(options) {
				this.selecValue2 = options.label
			},
			selectOne3(options) {
				this.selecValue3 = options.label
			},
			useOutClickSide() {
				this.$refs.easySelect.hideOptions && this.$refs.easySelect.hideOptions()
				this.$refs.easySelect1.hideOptions && this.$refs.easySelect1.hideOptions()
				this.$refs.easySelect2.hideOptions && this.$refs.easySelect2.hideOptions()
				this.$refs.easySelect3.hideOptions && this.$refs.easySelect3.hideOptions()
			}
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		overflow: scroll;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		margin-top: 50rpx;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
