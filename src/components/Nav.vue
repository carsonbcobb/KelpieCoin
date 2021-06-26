<template>
	<div class="nav">
		<div class="nav__logo">
			<img src="../assets/logo.png" />
		</div>

		<div class="nav__links">
			<a href="#hero" class="nav__links--link">Launchpad</a>
			<a href="#about" class="nav__links--link">About</a>
			<a href="#swap" class="nav__links--link">Tokenomics</a>
			<a href="#eco" class="nav__links--link">Ecosystem</a>
			<a href="#roadmap" class="nav__links--link">Roadmap</a>
			<a href="#network" class="nav__links--link">Network</a>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Nav',
};
</script>

<style scoped>
.nav {
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	align-content: center;
	border-top: 8px solid #f9da00;
	padding: 25px 100px;
}

.nav__logo img {
	max-block-size: 75px;
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
	color: white;
	border-bottom: 3px solid transparent;
	transition: 0.35s ease-in-out;
}

.nav__links--link:hover {
	color: #f9da00;
	border-bottom: 3px solid #f9da00;
}

@media (max-width: 1024px) {
	.nav__links--link {
		margin: 0 10px;
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
