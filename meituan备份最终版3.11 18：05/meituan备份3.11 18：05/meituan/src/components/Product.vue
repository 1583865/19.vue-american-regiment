<!-- 模板 -->
<template>
<div class="ickt-product">
	<router-link class="inner" tag="div" :to="'/homedetail/' + data.id">
		<img :src="'/img/list/' + data.img" alt="">
		<div class="content">
			<h3>{{data.title}}</h3>
			<p>
				<span class="price">{{data.price}}元</span>
				<span class="origin-price">门市价:{{data.originPrice}}元</span>
				<span class="sales">销量{{data.sales}}</span>
			</p>
		</div>
	</router-link>
</div>
</template>
<style type="text/css" lang="scss" scoped>
// 引入样式库
@import '../base.scss';
.ickt-product {
	.inner {
		margin: 0 10px;
		padding: 10px 0;
		border-bottom: 1px solid #ccc;
		display: flex;
		img {
			width: 100px;
			height: 60.5px;
		}
		.content {
			flex: 1;
			padding-left: 10px;
		}
		h3 {
			font-weight: 500;
			font-size: 16px;
			height: 43px;
		}
		p {
			font-size: 12px;
			color: #808487;
		}
		.price {
			color: $navColor;
			margin-right: 6px;
			font-size: 18px;
		}
		.sales {
			float: right;
		}
	}
}
</style>
<script type="text/javascript">
// 组件
export default {
	// 接收数据
	props: ['data'],
	// 创建完成
	// created() {
	// 	console.log(this)
	// }
}
</script>