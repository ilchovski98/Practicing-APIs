<template>
	<header class="header">
		<div class="header__inner">
			<div class="header__logo">
				<a href="#" class="logo">
					<img src="../../assets/logo.png">
				</a>
			</div><!-- /.header__logo -->

			<nav class="nav">
				<ul>
					<li>
						<a href="#">Bets</a>
					</li>

					<li>
						<a href="#">Messages</a>
					</li>

					<li>
						<a href="#">Login</a>
					</li>

					<li>
						<a href="#">Register</a>
					</li>
				</ul>
			</nav><!-- /.nav -->
		</div><!-- /.header__inner -->
	</header>
</template>

<script>
export default {
	name: "Header",
	props: [],
	data() {
		return {

		}
	}
}
</script>

<style>
	.header__logo img {
		max-width: 50px;
	}
	
	.header {
		padding: 20px 40px;
		background-color: #040404;
		color: #fff;
	}

	.header .header__inner {
		display: flex;
		justify-content: space-between;
		align-items: center;
		max-width: 1500px;
		margin: auto;
	}

	.nav ul {
		list-style-type: none;
		display: flex;
		margin-bottom: 0;
	}

	.nav li + li {
		margin-left: 20px;
	}

	.nav a {
		text-decoration: none;
		font-size: 16px;
		color: #fff;
		position: relative;
	}

	.nav a:hover {
		text-decoration: none;
		color: #fff;
	}

	.nav a:after {
		position: absolute;
		top: calc(100% + 2px);
		left: 0;
		right: 0;
		height: 2px;
		background-color: #32f0a4;
		transform: scaleX(0);
		transition: transform .4s;
		content: '';
	}

	.nav a:hover:after {
		transform: none;
	}
</style>