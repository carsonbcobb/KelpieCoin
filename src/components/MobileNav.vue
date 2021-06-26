<template>
	<div class="mobileNav">
		<div class="nav__logo">
			<img src="../assets/logo.png" />
		</div>

		<div class="nav__menu">
			<div id="menuButton" class="menuButton ">
				<ul class="menuButton-ul" aria-hidden="true">
					<li class="menuButton-li"></li>
					<li class="menuButton-li"></li>
					<li class="menuButton-li"></li>
				</ul>
			</div>

			<nav id="main-menu" hidden>
				<ul>
					<li><a class="main-menu--link" href="#hero">Launchpad</a></li>
					<li><a class="main-menu--link" href="#about">About</a></li>
					<li><a class="main-menu--link" href="#swap">Tokenomics</a></li>
					<li><a class="main-menu--link" href="#eco">Ecosystem</a></li>
					<li><a class="main-menu--link" href="#roadmap">Roadmap</a></li>
					<li><a class="main-menu--link" href="#network">Network</a></li>
				</ul>
			</nav>
		</div>
	</div>
</template>

<script>
import $ from 'jquery';

export default {
	name: 'MobileNav',
};
$(document).ready(function() {
	$('ul').click(function() {
		$(this).toggleClass('active');
	});
});
</script>

<style scoped>
.mobileNav {
	padding: 25px;
}
.nav__logo img {
	max-width: 100px;
}

@media (min-width: 768px) {
	.mobileNav {
		display: none;
	}
}

@media (max-width: 768px) {
	.mobileNav {
		display: block;
	}
}

.menuButton-ul {
	position: absolute;
	top: 60px;
	right: -50px;
	transform: translate(-50%, -50%);
	width: 75px;
	height: 75px;
	background: transparent;
	cursor: pointer;
}
.menuButton-ul .menuButton-li {
	list-style: none;
	display: inline-block;
	position: absolute;
	top: 50%;
	transform: translate(-50%, -50%);
	width: 20px;
	height: 20px;
	background: white;
	border-radius: 50%;
	border: none;
	transition: 0.9s;
}
.menuButton-ul .menuButton-li:nth-of-type(1) {
	left: 20%;
	z-index: 2;
}
.menuButton-ul .menuButton-li:nth-of-type(2) {
	transition: 1.2s;
	transition-delay: 0;
	left: 50%;
}
.menuButton-ul .menuButton-li:nth-of-type(3) {
	left: 80%;
	z-index: 2;
}

.menuButton-ul.active .menuButton-li:nth-of-type(1),
.menuButton-ul.active .menuButton-li:nth-of-type(3) {
	top: 50%;
	left: 50%;
	border-radius: 0;
	width: 6px;
	height: 60px;
	transition-delay: 0.8s;
}
.menuButton-ul.active .menuButton-li:nth-of-type(1) {
	transform: translate(-50%, -50%) rotate(405deg);
}
.menuButton-ul.active .menuButton-li:nth-of-type(3) {
	transform: translate(-50%, -50%) rotate(-405deg);
}
.menuButton-ul.active .menuButton-li:nth-of-type(2) {
	top: 50%;
	left: 50%;
	width: 70px;
	height: 70px;
	background: rgb(30, 5, 83);
	border: 3px solid #fada00;
}

.main-menu {
	position: absolute;
	display: none;
	left: -200px;
	top: 0;
	height: 100%;
	overflow-y: scroll;
	overflow-x: visible;
	transition: left 0.3s ease, box-shadow 0.3s ease;
	z-index: 999;
}

.main-menu {
	list-style: none;
	margin: 0;
	padding: 2.5em 0 0;
	/* Hide shadow w/ -8px while 'closed' */
	-webkit-box-shadow: -8px 0 8px rgba(0, 0, 0, 0.5);
	-moz-box-shadow: -8px 0 8px rgba(0, 0, 0, 0.5);
	box-shadow: -8px 0 8px rgba(0, 0, 0, 0.5);
	min-height: 100%;
	width: 200px;
	background: #1a1a1a;
}

.main-menu a {
	display: block;
	padding: 0.75em 15px;
	line-height: 1em;
	font-size: 1em;
	color: #fff;
	text-decoration: none;
	border-bottom: 1px solid #383838;
}

.main-menu li:first-child a {
	border-top: 1px solid #383838;
}

.main-menu a:hover,
.main-menu a:focus {
	background: #333;
	text-decoration: underline;
}

.main-menu .menu-close {
	position: absolute;
	right: 0;
	top: 0;
}
</style>
