<template>
<div class="mobileNav">
    <div class="nav__logo">
        <img src="../assets/logo.png" />
    </div>
    <div class="navigation" id="navigation">
        <input type="checkbox" v-model="checked" id="navi-toggle" class="navigation__checkbox" />

        <label for="navi-toggle" class="navigation__button">
            <span class="navigation__icon">
                <span class="navigation__icon-span">&nbsp;</span>
                <span class="navigation__icon-span">&nbsp;</span>
                <span class="navigation__icon-span">&nbsp;</span>
                <span class="navigation__icon-span">&nbsp;</span>
                <span class="navigation__icon-span">&nbsp;</span>
                <span class="navigation__icon-span">&nbsp;</span>
            </span>
        </label>

        <div class="navigation__background">&nbsp;</div>

        <nav class="navigation__nav">

            <ul class="navigation__list" id="nav-list">
                <div id="navmenu-img">
                    <img src="../assets/navmenu.png" />
                </div>
                <li class="navigation__item" @click="hideNav()">
                    <a href="#hero" class="navigation__link" @click="handleLinkClick">Launchpad</a>
                </li>
                <li class="navigation__item" @click="hideNav()">
                    <a href="#about" class="navigation__link" @click="handleLinkClick">About</a>
                </li>
                <li class="navigation__item" @click="hideNav()">
                    <a href="#swap" class="navigation__link" @click="handleLinkClick">Tokenomics</a>
                </li>

                <li class="navigation__item" @click="hideNav()">
                    <a href="#earn" class="navigation__link" @click="handleLinkClick">Earn</a>
                </li>
                <li class="navigation__item" @click="hideNav()">
                    <a href="#network" class="navigation__link" @click="handleLinkClick">Network</a>
                </li>

            </ul>

        </nav>
    </div>
</div>
</template>

<script>
export default {
    name: 'MobileNav',
    data() {
        return {
            checked: false,
        };
    },
    methods: {
        hideNav: function () {
            this.checked = false;
        },
        toggleScrollLock(event) {
            if (event.target.checked) {
                this.lockScroll();
            } else {
                this.unlockScroll();
            }
        },
		handleLinkClick(event) {
      event.preventDefault();
      const targetId = event.target.getAttribute('href').substring(1);
      const targetElement = document.getElementById(targetId);

      if (targetElement) {
        this.$emit('close');
        document.body.style.overflow = '';
        document.body.style.position = '';
        
        setTimeout(() => {
          targetElement.scrollIntoView({ behavior: 'smooth' });
        }, 500);
      }
    }
    }
};
</script>

<style scoped>
@keyframes background-animation {
    0% {
        background-position: 0% 50%;
    }

    50% {
        background-position: 100% 50%;
    }

    100% {
        background-position: 0% 50%;
    }
}

.mobileNav {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 200px;
    overflow: hidden;
    margin-bottom: 40px;
}

.nav__logo img {
    max-width: 60px;
    max-height: 60px;
    margin-top: 0px;
    margin-left: 10px;
    margin-top: 10px;
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

.heading-primary {
    color: #fff;
    text-transform: uppercase;
    backface-visibility: hidden;
    margin-bottom: 6rem;
}

.heading-primary--main {
    display: block;
    font-size: 6rem;
    font-weight: 400;
    letter-spacing: 3.5rem;
    margin-right: -3.5rem;
    animation-name: moveInLeft;
    animation-duration: 1s;
    animation-timing-function: ease-out;
}

.heading-primary--sub {
    display: block;
    font-size: 2rem;
    font-weight: 700;
    letter-spacing: 1.75rem;
    margin-right: -1.75rem;
    animation: moveInRight 1s ease-out;
}

.btn,
.btn:link,
.btn:visited {
    position: relative;
    display: inline-block;
    padding: 1.5rem 4rem;
    text-decoration: none;
    text-transform: uppercase;
    font-size: 1.6rem;
    border-radius: 5rem;
    backface-visibility: hidden;
    z-index: 0;
    transition: all 0.2s;
    border: none;
    cursor: pointer;
}

.btn::after {
    content: '';
    position: absolute;
    display: inline-block;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    border-radius: 5rem;
    z-index: -1;
    transition: all 0.4s;
}

.btn:hover,
.btn:focus {
    transform: translateY(-0.3rem);
    box-shadow: 0 1rem 2rem rgba(0, 0, 0, 0.2);
    outline: none;
}

.btn:hover::after,
.btn:focus::after {
    opacity: 0;
    transform: scaleX(1.4) scaleY(1.6);
}

.btn:active {
    transform: translateY(-0.1rem);
    box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.2);
}

.btn--white {
    background-color: #fff;
    color: #777;
}

.btn--white::after {
    background-color: #fff;
}

.btn--animated {
    animation: moveInBottom 0.5s ease-out 0.75s backwards;
}

@keyframes moveInLeft {
    0% {
        opacity: 0;
        transform: translateX(-10rem);
    }

    80% {
        transform: translateX(1rem);
    }

    100% {
        opacity: 1;
        transform: translateX(0);
    }
}

@keyframes moveInRight {
    0% {
        opacity: 0;
        transform: translateX(10rem);
    }

    80% {
        transform: translateX(-1rem);
    }

    100% {
        opacity: 1;
        transform: translateX(0);
    }
}

@keyframes moveInBottom {
    from {
        opacity: 0;
        transform: translateY(3rem);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

#navmenu-img {
    margin: 25px auto 0 auto;

}

#navmenu-img img {
    width: 200px;
}

.navigation__checkbox {
    display: none;
}

.navigation__checkbox:checked~.navigation__background {
    transform: scale(100);
    width: 100vw;
    height: 100vh;
}

.navigation__checkbox:checked~.navigation__nav {
    transform: translateX(0);
    visibility: initial;
    opacity: 1;
    width: 100vw;
    height: 100vh;
}


.navigation__button {
    position: absolute;
    top: 10px;
    right: 10px;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background: #FFA500;
    background-size: 400% 400%;
    animation: background-animation 10s ease infinite;
    z-index: 10;
    box-shadow: 0 1rem 3rem rgba(0, 0, 0, 0.2);
    cursor: pointer;
    z-index: 12;
    text-align: center;
}

.navigation__button::after {
    background: white;
}

.navigation__background {
    position: absolute;
    top: 10px;
    right: 10px;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background: #8B4513;
    background-size: 400% 400%;
    animation: background-animation 10s ease infinite;
    z-index: 10;
    transition: transform 0.8s cubic-bezier(0.86, 0, 0.07, 1);
}

.navigation__nav {
    position: absolute;
    top: 0;
    left: 0;
    height: 100vh;
    width: 100%;
    z-index: 11;
    transform: translateX(-50%);
    visibility: hidden;
    opacity: 0;
    transition: opacity 0.8s ease-in,
        transform 0.8s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

.navigation__list {
    text-align: center;
    list-style: none;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-family: "Fredoka", sans-serif;
    padding: 0;
    margin: 0;
}

.navigation__item {
    margin: 15px 0;

    font-family: "Fredoka", sans-serif;
}

.navigation__link::before {
    padding-right: 1.2rem;
}

.navigation__link:link,
.navigation__link:visited {
    display: inline-block;
    font-size: 1.5rem;
    font-weight: normal;
    padding: .75rem 2rem;
    color: #fff;
    text-decoration: none;
    text-transform: uppercase;
    background-image: linear-gradient(120deg,
            transparent 0%,
            transparent 49.9%,
            #FFA500 50%);
    background-size: 227%;
    transition: all 0.4s;
}

.navigation__link:hover,
.navigation__link:active {
    color: white;
    background-position: 100%;
    transform: translateX(1rem);
}

.navigation__icon {
    display: inline-block;
    position: relative;
    width: 1.75rem;
    height: 0.3rem;
    top: 30%;
    transition: transform 0.25s ease-in-out;
}

.navigation__icon-span {
    position: absolute;
    height: 0.2rem;
    width: 50%;
    background: rgba(250, 250, 250, .75);
    transition: all 0.5s ease-in;
}

.navigation__icon-span:nth-child(even) {
    left: 50%;
    border-radius: 0 0.9rem 0.9rem 0;
}

.navigation__icon-span:nth-child(odd) {
    left: 0;
    border-radius: 0.9rem 0 0 0.9rem;
}

.navigation__icon-span:nth-child(1),
.navigation__icon-span:nth-child(2) {
    transform: translateY(-.65rem);
}

.navigation__icon-span:nth-child(5),
.navigation__icon-span:nth-child(6) {
    transform: translateY(.65rem);
}

.navigation__checkbox:checked+.navigation__button .navigation__icon-span:nth-child(1),
.navigation__checkbox:checked+.navigation__button .navigation__icon-span:nth-child(6) {
    transform: rotate(45deg);
}

.navigation__checkbox:checked+.navigation__button .navigation__icon-span:nth-child(2),
.navigation__checkbox:checked+.navigation__button .navigation__icon-span:nth-child(5) {
    transform: rotate(-45deg);
}

.navigation__checkbox:checked+.navigation__button .navigation__icon-span:nth-child(2),
.navigation__checkbox:checked+.navigation__button .navigation__icon-span:nth-child(6) {
    transform-origin: left;
}

.navigation__checkbox:checked+.navigation__button .navigation__icon-span:nth-child(1),
.navigation__checkbox:checked+.navigation__button .navigation__icon-span:nth-child(5) {
    transform-origin: right;
}

.navigation__checkbox:checked+.navigation__button .navigation__icon-span:nth-child(3) {
    left: -50%;
    opacity: 0;
}

.navigation__checkbox:checked+.navigation__button .navigation__icon-span:nth-child(4) {
    left: 100%;
    opacity: 0;
}

.navigation__button:hover .navigation__icon-span:nth-child(3) {
    transform: translateX(-0.3rem) scale(1.1);
}

.navigation__button:hover .navigation__icon-span:nth-child(4) {
    transform: translateX(0.3rem) scale(1.1);
}

.navigation__checkbox:checked+.navigation__button:hover .navigation__icon {
    transform: rotate(180deg) translateY(25%);
}

.header {
    background-image: linear-gradient(to right bottom, #7ed56f, #28b485);
    height: 95vh;
    position: relative;
    clip-path: polygon(0 0, 100% 0, 100% 75vh, 0 100%);
}

.header__text-box {
    position: absolute;
    top: 40%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
}

.navigation__checkbox:checked {
    overflow: hidden;
}

@media (max-width: 435px) {

    .navigation__button,
    .navigation__background {
        right: 10px;
    }
}
</style>
