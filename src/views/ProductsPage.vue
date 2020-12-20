<template>
	<div class="container" style="zoom: 75%">
		<div class="row">
			<div v-for="product in products"
			     class="product-item col-sm-3"
			     v-bind:key="product.id"
			>
				<img v-bind:src="product.imageUrl"/>
				<h3 class="product-name">{{ product.name }}</h3>
				<p class="product-price">${{ product.price }}</p>
				<router-link v-bind:to="'/products/' + product.id">
					<button class="view-details btn btn-dark"> View Details</button>
				</router-link>
			</div>
		</div>
	</div>
</template>

<script>
import {products} from '../fake-data.js'

export default {
    name: 'ProductsPage',
    data() {
        return {
            products
        }
    },
}
</script>

<style scoped>
	.product-item {
		border: 1px solid lightgray;
		margin: 2px;
	}
	.product-item h3{
		font-weight: bold;
	}
	.view-details{
		width: 70%;
	}
</style>
