<template>
	<header class="header-secondary">
		<div class="header__inner">
			
		</div><!-- /.header__inner -->
	</header>
</template>

<script>

export default {
	name: "Header-secondary",
	props: [],
	data() {
		return {

		}
	}
}
</script>

<style>
	.header-secondary {
		background-color: #32f0a4;
		padding: 10px 0;
	}

	.header-secondary .header__inner {
		display: flex;
		justify-content: center;
	}

	.stock {
		display: flex;
		align-items: center;
	}
</style>