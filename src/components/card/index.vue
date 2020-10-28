<template>
	<div class="card-price">
		<div class="card__content">
			<h5 class="card__name">
				<slot name="card__name"></slot>
			</h5><!--/.card__name -->

			<h6 class="card__price">
				<slot name="card__price"></slot>
			</h6><!--/.card__price -->
			
			<div class="card__entry">
				<slot name="card__entry"></slot>
			</div><!--/.card__entry -->
		</div><!--/.card__content -->
	</div><!--/.card-prce -->
</template>

<script>
	export default {
		name: "Card",
		props: [],
		data() {
			return {

			}
		}
	}
</script>

<style>
	.card-price {
		border: 1px solid #000;
		width: 300px;
		min-height: 200px;
		border-radius: 20px;
	}

	.card-price .card__content {
		padding: 10px;
	}

	.card-price .card__name {
		font-size: 20px;
		font-weight: bold;
		font-family: 'Roboto';
		text-align: center;
	}

	.card-price .card__price {
		font-size: 16px;
		font-weight: 500;
		color: #403f3c;
		text-align: center;
	}

	.card-price .card__entry {
		font-size: 12px;
		line-height: 1.6;
	}
</style>