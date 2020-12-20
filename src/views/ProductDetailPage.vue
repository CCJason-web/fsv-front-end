<template>
	<div id="page-wrap" style="zoom: 75%">
		<div id="img-wrap">
			<img v-bind:src="product.imageUrl" />
		</div>
		<div id="product-details">
			<h1>{{ product.name }}</h1>
		</div>
	</div>
</template>

<script>
import {products} from '../fake-data';

export default {
    name: 'ProductDetailPage',
	data() {
        return {
          product: products.find((p) => p.id === this.$route.params.id )
        }
	}
}
</script>

<style scoped>
h1 {
	color: red;
}
</style>
