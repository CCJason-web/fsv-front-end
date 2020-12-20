<template>
	<div>
		<ProductsGridItem
		class="product-item col-sm-3"
		v-for="product in products"
		:key="product.id"
		:product="product"/>
	</div>
</template>
<script>
import ProductsGridItem from './ProductsGridItem'

export default {
    name: 'ProductsGrid',
	props: ['products'],
    components: {
        ProductsGridItem
    }
}
</script>
<style scoped>
	.product-item {
		border: 1px solid lightgray;
		margin: 2px;
	}


</style>
