<template>
	<div id="page-wrap" style="zoom: 75%" v-if="product">
		<div id="img-wrap">
			<img v-bind:src="product.imageUrl" />
		</div>
		<div id="product-details">
			<h1>{{ product.name }}</h1>
		</div>
		<div id="product-prices">
			<p>${{ product.price }}</p>
		</div>
		<button class="btn btn-dark">Buy</button>
	</div>
	<NotFoundPage v-else/>
</template>

<script>
import {products} from '../fake-data';
import NotFoundPage from './NotFoundPage'

export default {
    name: 'ProductDetailPage',
    components: {NotFoundPage},
    data() {
        return {
          product: products.find((p) => p.id === this.$route.params.id )
        }
	}
}
</script>

<style scoped>
	#page-wrap {
		border: 1px solid lightgray;
		margin: 2px;
	}
</style>
