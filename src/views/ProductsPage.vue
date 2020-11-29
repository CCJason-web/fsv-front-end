<template>
	<div class="page-wrap">
		<div class="group-wrap">
			<div v-for="product in products"
			     class="product-item"
			     v-bind:key="product.id"
			>
				<img v-bind:src="product.imageUrl"/>
				<h3 class="product-name">{{ product.name }}</h3>
				<p class="product-price">${{ product.price }}</p>
				<router-link v-bind:to="'/products/' + product.id">
					<button>View Details, Haha</button>
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

</style>
