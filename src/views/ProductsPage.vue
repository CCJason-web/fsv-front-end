<template>
	<div class="container" style="zoom: 75%">
		<div class="row">
			<ProductsGrid :products="products"/>
		</div>
	</div>
</template>

<script>
import {products} from '../fake-data.js'
import ProductsGrid from '../components/ProductsGrid'

export default {
    name: 'ProductsPage',
	components: {
        ProductsGrid
    },
    data() {
        return {
            products
        }
    },
}
</script>


