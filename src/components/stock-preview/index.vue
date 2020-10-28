<template>
	<div class="stock-preview">
		<span class="stock__price">
			<slot name="price"></slot>
		</span>
	</div><!-- /.stock-preview -->
</template>

<script>

export default {
	name: "Stock-preview",
	props: [],
	data() {
		return {

		}
	}
}
</script>

<style>
	.stock-preview .stock__image {
		max-width: 30px;
	}

	.stock-preview .stock__price {
		margin-left: 10px;
		font-weight: bold;
		color: #fff;
		text-shadow: 1px 1px 1px #000;
	}
</style>