<template>
	<div class="nav">
		<div class="nav__logo">
			<img src="../assets/logo.png" />
		</div>

		<div class="nav__links">
			<a href="#hero" class="nav__links--link">Launchpad</a>
			<a href="#about" class="nav__links--link">About</a>
			<a href="#swap" class="nav__links--link">Tokenomics</a>
			<a href="#earn" class="nav__links--link">Earn</a>
			<a href="#network" class="nav__links--link">Network</a>
		</div>
	</div>
</template>

<script>
export default {
	name: 'AppNavigation',
};
</script>

<style scoped>
.nav {
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	align-content: center;
	padding: 5px 100px;
	background: rgba(265,265,265, .9);
	margin: auto;
	max-width: 1440px;
}

.nav__logo img {
	max-block-size: 50px;
}

.nav__links {
	display: flex;
	justify-content: space-evenly;
	align-items: center;
}

.nav__links--link {
	margin: 0 30px;
	font-size: 1.15rem;
	text-decoration: none;
	font-weight: normal;
	color: #8B4513;
	border-bottom: 2px solid transparent;
	transition: 0.35s ease-in-out;
	cursor: pointer;
	font-family: "Fredoka", sans-serif;

}

.nav__links--link:hover {
	border-bottom: 2px solid #FFA500;
}

@media (max-width: 1024px) {
	.nav__links--link {
		margin: 0 15px;
	}

	.nav {
		padding: 25px;
	}
}

@media (max-width: 768px) {
	.nav__links--link {
		margin: 0 10px;
		font-size: 0.8rem;
	}

	.nav {
		padding: 25px;
	}
}

@media (max-width: 768px) {
	.nav {
		display: none;
	}
}
</style>
