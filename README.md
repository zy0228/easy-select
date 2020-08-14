# easy-select (小程序版uniapp)
### Basic example
```
<template>
	<view class="content" @click="useOutClickSide">
		<easy-select ref="easySelect" size="medium" :value="selecValue" @selectOne="selectOne"></easy-select>
	</view>
</template>

<script>
export default {
	data() {
		selecValue: '双皮奶'
	},
	methods: {
		selectOne(options) {
			this.selecValue = options.label
		},
		useOutClickSide() {
			this.$refs.easySelect.hideOptions && this.$refs.easySelect.hideOptions()
		}
	}
}
</script>
```
---
### Motivation
*小程序的picker组件其实已经满足了选择类型的需求场景, 而且我个人也觉得picker交互也很好。但是现实开发中可能产品或者设计并不希望你使用picker, 那么小程序又不支持select, 所以我个人认为, 我写的这个select只是你无法抗拒产品的意见时候的选择。大部分情况下还是picker比较符合移动端的操作*
___
### Options:
| props            | type    | require | explain                               |
| ---------------- | ------- | ------- | ------------------------------------- |
| windowHeight     | Num,str | false   | 可用视口的高度，如果没传入会自动帮你计算 |                             |
| value            | String  | false   | 当前选中的值                    |
| placeholder      | String  | false   | 提示文字                 |
| size       			 | String  | false   | 可选'medium, small, mini'尺寸           |
| options          | Array   | false   | options选项数据                    |
---
### Notice
+ options的格式：仿照[Element-ui](https://element.eleme.cn/#/zh-CN/component/select)element-ui的select格式即可
+ 完全的尺寸定制化.你可以直接这样来修改, 或者使用我们提供的三种尺寸
```
<easy-select style="width: 300px;heght: 200px"></easy-select>
```
---
### finally
同样的如果你可以，也鼓励你可以在我的基础上自己魔改~
另外这是我另外一个作品, 同样的好用快捷强大[easy-tabBar](https://ext.dcloud.net.cn/plugin?id=2221)。
最后，如果喜欢的话github地址 [github](https://github.com/zy0228/easy-select) 点个赞吧
