<template>
<div>
  <section id="hero">
    <Nav />
    <MobileNav />
    <div class="hero">
      <HeroBackgroundAnimation />

      <div class="hero__content">
        <h1 class="hero__content--header">
          Kelpie Coin<br />
          <span class="yellow">$KLP</span>
        </h1>
        <h2 class="hero__content--subheader desk">
          Kelpie Coin is a frictionless yield<br /> and liquidity generation protocol
          <br /> on the Solana Network.
        </h2>
        <h2 class="hero__content--subheader mob">
          Kelpie Coin is a frictionless yield and liquidity generation protocol
          on the Solana Network.
        </h2>

        <div class="hero__content--buttonGroup">
          <div class="button hero__button">
            <a href="https://www.dexlab.space/swap?id=3GQKSGznA6AkyAnhTQorUCwsu811z9hptAvm43Eszcmx" target="_blank" rel="norefferer">Trade on DexLab</a>
						
          </div>
        </div>
							

      </div>
      <div class="hero__image">
        <img src="./assets/hero.png" class="float-animation" />
      </div>

    </div>

  </section>
  <section id="about">
    <div class="about">
      <div class="about__header">
        <div class="about__header--img">
          <img src="./assets/logo.png" />
        </div>
        <h2>About Kelpie Coin</h2>
      </div>
      <div class="underline about-underline"></div>
      <div class="about__content">
        <p>
          Kelpie Coin is a frictionless yield and liquidity generation
          protocol that will help
          the token holders earn passive income while also enhancing the
          liquidity of the pool in the near future. This will be funded by 5% of the
          transaction fee taken from each transaction. This protocol has
          a permanently increasing-price floor, with all investors earning
          additional Kelpie Coin tokens for just holding it.
        </p>

      </div>
    </div>

    <div class="swap" id="swap">
      <div class="swap__header">
        <div class="swap__header--img">
          <img src="./assets/logo.png" />
        </div>
        <h3>KELPIE COIN</h3>
      </div>

      <div class="swap__section">
        <div class="swap__section--item">
          <p class="item-1">Total Supply</p>
          <p class="item-2 yellow">XXX</p>
        </div>

        <div class="swap__section--item">
          <p class="item-1">Ticker</p>
          <p class="item-2 yellow">$KLP</p>
        </div>

        <div class="swap__section--item">
          <p class="item-1">Exchange</p>
          <p class="item-2 yellow">DexLab</p>
        </div>

        <div class="swap__section--item">
          <p class="item-1">Donation to Charity</p>
          <p class="item-2 yellow">2%</p>
        </div>
        <div class="swap__section--item">
          <p class="item-1">Tax</p>
          <p class="item-2 yellow">1%</p>
        </div>
        <div class="swap__section--item">
          <p class="item-1">Reward to Holders</p>
          <p class="item-2 yellow">2%</p>
        </div>

      </div>
    </div>

    <div class="audit">
      <div class="audit__image">
        <img src="./assets/new-audit.png" />
      </div>

      <div class="audit__content">
        <h3 class="ghost">Audits</h3>
        <h4><span class="yellow">Kelpie Coin</span> Smart Contract Audit</h4>

        <p>
          Our Kelpie Coin token protocol is being audited by Certik, SGE,
          Techrate, Solidity, etc. We believe they will not find any high or
          medium security issues in the Smart Contract code. Our Smart
          Contract code is developed by one of the world's most proficient
          blockchain developers.
        </p>
        <div class="button button-inactive">
          <a>REPORT COMING SOON</a>
        </div>
      </div>

    </div>

    <div class="earn" id="earn">
      <div class="earn__content">
        <div class="earn__image tablet">
          <img src="./assets/audit.png" />
        </div>
        <h3 class="ghost">Earn</h3>
        <h4><span class="yellow">Earn</span> Passive Income</h4>
        <p>
          Gain $KLP every time a transaction is made. Our protocol charges a
          5% transaction fee; this means 1% goes into a locked liquidity pool
          , 2% is rewarded to our stakeholders, and 2% is donated a charity supporting Australian Kelpies. No need to trade, simply
          watch your balance increase in real-time. This is called a
          deflationary currency and will earn up to 80% annual yield
          percentage - exceptionally higher than any traditional savings
          account.
        </p>
        <div class="button">
          <a href="https://www.dexlab.space/swap?id=3GQKSGznA6AkyAnhTQorUCwsu811z9hptAvm43Eszcmx" target="_blank" rel="norefferer">Trade on DexLab</a>
        </div>

      </div>

      <div class="earn__image desk-img">
        <img src="./assets/audit.png" />
      </div>
    </div>
  </section>

  <div class="end_bg">
    <section id="network">
      <div class="network">
        <h2>Our Network</h2>
        <div class="underline"></div>
        <div class="network__image--container">
          <a class="network__image" href="https://solana.com/" target="_blank">
            <img src="./assets/sol.svg" />
          </a>
          <div class="vertical-line"></div>
          <a class="network__image" href="https://www.dexlab.space/" target="_blank">
            <img src="./assets/dexlab.png" />
          </a>
        </div>
      </div>
    </section>

    <div class="footer">
      <p>Copyright © 2021 All Rights Reserved.</p>
    </div>
  </div>
</div>
</template>

<script>
import Nav from './components/Nav.vue';
import MobileNav from './components/MobileNav.vue';
import HeroBackgroundAnimation from './components/HeroBackgroundAnimation.vue';

export default {
  name: 'App',

  components: {
    Nav,
    MobileNav,
    HeroBackgroundAnimation
  },
};
</script>

<style>
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

@keyframes float {
  0% {
    transform: translateY(0%);
  }

  40% {
    transform: translateY(8%);
  }

  80% {
    transform: translateY(-8%);
  }

  100% {
    transform: translateY(0%);
  }
}

html {
  background: white;
  font-family: 'Poppins', sans-serif;
  overflow-x: hidden;
  scroll-behavior: smooth;

  font-family: 'Roboto Mono', monospace;
}

body {
  max-width: 1440px;
  margin: auto;
  overflow-x: hidden;
  scroll-behavior: smooth;
  background: transparent;
}

#hero {}

.hero {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  padding: 50px 0;

}

.hero__content {
  color: black;
  margin-top: -100px;
  margin-left: -100px;
}

.hero__content--header {
  font-size: 3.5rem;
  font-weight: normal;
}

.hero__content--buttonGroup {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.hero__button {
  width: 50% !important;
  text-align: center;
}

.button {
  background: linear-gradient(45deg,
      rgb(30, 5, 83),
      rgb(78, 17, 158),
      rgb(65, 9, 105),
      rgb(78, 17, 158),
      rgb(30, 5, 83));
  background-size: 400% 400%;
  animation: background-animation 10s ease infinite;
  border-radius: 100px;
  border: 1px solid #fada00;
  padding: 15px;
  cursor: pointer;
  transition: 0.35s ease-in-out;
  width: fit-content;
}

.button a {
  color: white;
  font-weight: normal;
  font-size: 1.25rem;
  text-decoration: none;
  margin: 0 25px;
}

.button:hover::before {
  background: linear-gradient(45deg,
      rgb(30, 5, 83),
      rgb(78, 17, 158),
      rgb(65, 9, 105),
      rgb(78, 17, 158),
      rgb(30, 5, 83));
  background-size: 400% 400%;
  animation: background-animation 10s ease infinite;
  border: 1px solid #fada00;
  color: white;

}

.button:hover {
  background: linear-gradient(45deg,
      rgb(30, 5, 83),
      rgb(78, 17, 158),
      rgb(65, 9, 105),
      rgb(78, 17, 158),
      rgb(30, 5, 83));
  transform: scale(.95);
  background-size: 400% 400%;
  animation: background-animation 10s ease infinite;
  border: 1px solid transparent;

}

.button:active {}

.button-inactive {
  background: #3f3749;

}

.button-inactive:hover {
  background: #3f3749;
  border: 1px solid transparent;
  color: white;
  transform: scale(.95);

}

.yellow {
  color: #fada00;
}

.hero__image img {
  width: 400px;
  animation: float 10s ease-in-out 0.5s infinite;
}

.tablet {
  display: none;
}

.mob {
  display: none;
}



@media (max-width: 1024px) {
  .hero__content--header {
    font-size: 2.5rem;
  }

  .hero__image img {
    width: 300px;
  }

}

@media (max-width: 768px) {
  .hero {
    margin-top: 100px;
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
  }

  .hero__content {
    margin-bottom: 50px;
    margin-left: 0;
  }

  .hero__content--subheader {
    margin: 50px auto;
  }

  .hero__content--header {
    width: fit-content;
    margin: auto;
  }

  .hero__button {
    margin: auto;
  }

  .tablet {
    display: block;
  }

  .desk-img {
    display: none;
  }

	.center {
	text-align: center !important;
}

}

@media (max-width: 425px) {
  .hero__content--header {
    font-size: 2.5rem;
  }

  .hero__content--header span {
    font-size: 2rem;
  }

  .hero__content--subheader {
    text-align: justify;
    width: 80%;
    font-size: 1.05rem;
    margin: 50px auto;
  }

  .hero__content {
    font-size: 1rem;
    padding: 0 10px;
  }

  .hero__button a {
    font-size: 1.05rem;
  }

  .button {
    padding: 15px;
    background: linear-gradient(to top, #45108a, #12054e);
    border-radius: 100px;
    border: 2px solid #fada00;
    color: white;
    font-weight: bolder;
    font-size: 0.9rem;
    text-decoration: none;
    transition: 0.35s ease-in-out;
  }

  .mob {
    display: block;
  }

  .desk {
    display: none;
  }
}

/* About */
#about {
  margin-top: 50px;
  color: black;
}

.about {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 100px 0;

  background: url('./assets/about-bg.png'), #fff;
  background-size: 100% auto;
  background-repeat: no-repeat;
  background-position: center;
}

.about__header {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  text-align: center;
  font-weight: lighter;
  font-size: 1.75rem;
}

.about__header h2 {
  font-weight: lighter;
}

.about__header--img img {
  max-width: 50px;
  padding-right: 25px;
}

.about__content {
  font-size: 1.2rem;
  line-height: 2;
  margin-bottom: 100px;
}

.about__content p {
  width: 70%;
  margin: auto;
  text-align: justify;
}

@media (max-width: 1024px) {
  .about-underline {
    margin-bottom: 75px !important;
  }

  .about__content p {
    width: 80%;
  }
}

@media (max-width: 768px) {
  .about__content {
    padding: 0 20px;
  }
}

@media (max-width: 425px) {
  .about__header {
    display: flex;
    flex-direction: column;
    font-size: 1.5rem;
  }

  .about__header--img img {
    max-width: 100px;
    padding-right: 0px;
  }

  .about__content p {
    font-size: 1rem;
  }
}

/* SWAP */

.swap {
  background: linear-gradient(45deg,
      rgb(30, 5, 83),
      rgb(78, 17, 158),
      rgb(65, 9, 105),
      rgb(78, 17, 158),
      rgb(30, 5, 83));
  background-size: 400% 400%;
  animation: background-animation 10s ease infinite;
  margin: -150px 50px 0 50px;
  border-radius: 25px;
  padding: 25px;
  z-index: 20000 !important;
  box-shadow: 0px -5px 5px 0px #333;
  color: white;
  border: 1px solid rgba(250, 218, 0, 1);
}

.swap__header {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-bottom: 50px;
  font-size: 1.25rem;
  letter-spacing: 2px;
  word-spacing: 3px;
}

.swap__header--img img {
  max-width: 75px;
}

.swap__section {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  text-align: center;
  font-size: 1.1rem;

  background: url('./assets/swap.png');
  background-size: contain;
  background-repeat: no-repeat;
  background-position: 500px 50px;
  padding-bottom: 50px;
}

.swap__section--item {
  margin: 30px 0;
}

.item-2 {
  background: #12054e;
  width: 150px;
  margin: auto;
  padding: 15px 25px;
  border-radius: 15px;
}

.blue {
  color: #26e8ff;
}

@media (max-width: 1024px) {
  .swap {
    padding: 25px 0;
  }

  .swap__section {
    background-position: 200px 0px;
  }
}

@media (max-width: 768px) {
  .swap__section {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr;

    background-position: 0px 200px;
  }
}

@media (max-width: 425px) {
  .swap__section {
    grid-template-columns: 1fr;
    grid-template-rows: 1fr 1fr 1fr 1fr 1fr;
    text-align: center;
    font-size: 1.1rem;
    background-size: 1500px;
    background-position: bottom;
  }

  .swap__header {
    margin: auto;
    text-align: center;
  }

  .swap {
    padding: 25px 0;

  }
}

/* AUDIT */

.audit {
  background: white;

  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

.audit__image img,
.earn__image img {
  max-width: 600px;
}

.audit__content {
  margin-left: 200px;
}

.earn__content {
  transform: translateX(-25%);
}

.audit__content h3,
.earn__content h3 {
  font-size: 3rem;
  margin-bottom: -25px;
  opacity: 0.09;
}

.audit__content h4,
.earn__content h4 {
  font-size: 2rem;
  margin-bottom: 0px;
}

.audit__content p,
.earn__content p {
  font-size: 1.25rem;
  margin-bottom: 50px;
  line-height: 2;
}

.earn {
  background: white;

  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}

.earn__content {
  margin-left: 200px;
}

.mob-img {
  display: none;
}

@media (max-width: 1024px) {

  .audit__image img,
  .earn__image img {
    max-width: 450px;
  }

  .audit__content,
  .earn__content {
    margin: 0 25px;
  }

  .audit__content p,
  .earn__content p {
    text-align: justify;
    font-size: 1.15rem;
  }

	.earn__content {
  transform: translateX(0%);
}
}

@media (max-width: 768px) {

  .audit,
  .earn {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    margin-top: 50px;
  }

  .audit__image,
  .earn__image {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .audit__image img,
  .earn__image img {
    max-width: 500px;

  }

  .earn__image img {
    margin-left: -100px;
  }

	.earn__content {
    transform: translateX(0%);
}

  .desk-img {
    display: none;
  }

  .mob-img {
    padding-top: 50px;
    display: block;
  }

  .audit .button,
  .earn .button {
    margin: auto;
  }

  .audit__content h3,
  .earn__content h3 {
    margin: auto;
    width: fit-content;
  }

  .audit__content h4,
  .earn__content h4 {
    margin: auto;
    width: fit-content;

  }
}

@media (max-width: 425px) {

  .audit,
  .earn {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .audit__image img,
  .earn__image img {
    max-width: 350px;
  }

  .audit__content h3,
  .earn__content h3 {
    text-align: center;
  }

  .audit__content h4,
  .earn__content h4 {
    text-align: center;

  }
}

/*ROADMAP*/

.end_bg {
  color: black;
}

.roadmap {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: white;
}

.roadmap h2 {
  font-size: 2rem;
  font-weight: lighter;
  color: black;
}

.roadmap__image img {
  max-width: 100%;
}

@media (max-width: 425px) {
  .roadmap__image img {
    max-width: 80%;
  }
}

/* Network */

.network {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-top: 150px;
  text-align: center;
}

.network h2 {
  font-size: 2rem;
  color: black;
  font-weight: lighter;
}

.network__image--container {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  padding: 75px 50px;
  width: 100%;
}

.network__image img {
  max-width: 250px;
}

.vertical-line {
  height: 400px;
  width: 1px;
  background: #fada00;
}

.footer {
  text-align: center;
  padding: 0 0 20px 0;
  color: rgba(255, 255, 255, 0.5);
  border-bottom: 5px solid #fada00;
}

@media (max-width: 1024px) {
  .network__image img {
    max-width: 200px;
  }
}

@media (max-width: 768px) {
  .network__image img {
    max-width: 150px;
  }

  .vertical-line {
    height: 300px;
    width: 1px;
    background: #fada00;
  }
}

@media (max-width: 425px) {
  .network__image--container {
    flex-direction: column;
  }

  .vertical-line {
    height: 1px;
    width: 300px;
    background: #fada00;
    margin: 50px 0;
  }
}
</style>
