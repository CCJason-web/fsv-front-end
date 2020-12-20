<template>
	<div class="container" style="zoom: 75%">
		<h1 class="justify-content-lg-end text-left">Shopping Cart</h1>
		<div v-for="product in cartItems"
		     class="product-item row"
		     v-bind:key="product.id"
		>
			<img v-bind:src="product.imageUrl" class="col-2">
			<div class="col-8 text-left align-self-center">
				<h3 class="product-name">{{product.name}}</h3>
				<p class="product-price">${{product.price}}</p>
			</div>
			<button class="remove-button btn btn-dark col-2 align-self-center">Remove From Cart</button>
		</div>
		<h3 id="total-price" class="text-right">Total: ${{ totalPrice }}</h3>
		<button id="checkout-button" class="btn btn btn-dark col">Proceed to Checkout</button>
	</div>
</template>

<script>
import {cartItems} from '../fake-data'

export default {
    name: 'CartPage',
    data() {
        return {
            cartItems
        }
    },
    computed: {
        totalPrice() {
            return this.cartItems.reduce(
                (sum, item) => sum + Number(item.price),
                0
            )
        }
    }
}
</script>

<style scoped>
	h1 {
		border-bottom: 1px solid black;
		margin: 0;
		margin-top: 16px;
		padding: 16px;
	}

	img {
		width: 50%;
		height: 50%;
	}

	.product-item .remove-button {
		width: 28.75%;
		height: 10%;
	}
</style>
