<template>
	<div class="container ">
		<div id="nav-bar" class="navbar-collapse row">
			<router-link to="/products" id="products-link" class="col text-left ">
				<h1>FABULOUS FOOTWEAR</h1>
			</router-link>
			<router-link to="/cart" id="cart-link">
				<div class="col">
					<button class="btn btn-dark">Shopping Cart</button>
					<a href="javascript:void(0)" class="link-login btn btn-dark disabled">Login</a>
				</div>
			</router-link>
		</div>
	</div>
</template>

<script>
export default {
    name: 'NavBar',
}
</script>

<style scoped>
	#products-link {
		color: black;
		font-weight: bold;
	}
	.link-login {
		/*padding-left: 1px;*/
	}
</style>
