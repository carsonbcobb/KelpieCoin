<template >
  <div>
    <section id="hero">
      <AppNavigation />
      <MobileNav />
      <div class="hero">
        <HeroBackgroundAnimation />

        <div class="hero__content">
          <h1 class="hero__content--header">
            Kelpie Coin<br />
            <span class="highlight">$KLP</span>
          </h1>
       
          <h2 class="hero__content--subheader">
            Kelpie Coin is a frictionless yield and liquidity generation protocol
            on the Solana Network.
          </h2>

          <div class="hero__content--buttonGroup">
            <a href="https://www.dexlab.space/swap?id=3GQKSGznA6AkyAnhTQorUCwsu811z9hptAvm43Eszcmx" target="_blank" rel="noopener noreferrer" class="button hero__button">
              Trade on DexLab
            </a>
          </div>
        </div>
        <div class="hero__image">
          <img src="./assets/hero.png" class="float-animation" alt="Hero Image" />
        </div>
      </div>
    </section>

    <section id="about">
      <div class="about">
        <div class="about__header">
          <div class="about__header--img">
            <img src="./assets/logo.png" alt="Kelpie Coin Logo" />
          </div>
          <h2>About Kelpie Coin</h2>
        </div>
        <div class="underline about-underline"></div>
        <div class="about__content">
          <p>
            Kelpie Coin is a frictionless yield and liquidity generation protocol that will help
            the token holders earn passive income while also enhancing the liquidity of the pool in the near future. This will be funded by 5% of the
            transaction fee taken from each transaction. This protocol has a permanently increasing-price floor, with all investors earning
            additional Kelpie Coin tokens for just holding it.
          </p>
        </div>
      </div>

      <div class="swap" id="swap">
        <div class="swap__header">
          <div class="swap__header--img">
            <img src="./assets/logo.png" alt="Kelpie Coin Logo" />
          </div>
          <h3>KELPIE COIN</h3>
        </div>
        <p id="token-url">Token Address: CerCpUTyYsyEJiq33X2dReEfXPQ5JonJFS9Pzd6u2F55</p>

        <div class="swap__section">
          <div class="swap__section--item">
            <p class="item-1">Total Supply</p>
            <p class="item-2 highlight">1,239,184,931</p>
          </div>
          <div class="swap__section--item">
            <p class="item-1">Ticker</p>
            <p class="item-2 highlight">$KLP</p>
          </div>
          <div class="swap__section--item">
            <p class="item-1">Exchange</p>
            <p class="item-2 highlight">DexLab</p>
          </div>
          <div class="swap__section--item">
            <p class="item-1">Donation to Charity</p>
            <p class="item-2 highlight">2%</p>
          </div>
          <div class="swap__section--item">
            <p class="item-1">Tax</p>
            <p class="item-2 highlight">1%</p>
          </div>
          <div class="swap__section--item">
            <p class="item-1">Reward to Holders</p>
            <p class="item-2 highlight">2%</p>
          </div>
          
        </div>
      </div>

      <div class="audit">
        <div class="audit__image">
          <img src="./assets/new-audit.png" alt="Audit Image" />
        </div>
        <div class="audit__content">
          <h3 class="ghost">Audits</h3>
          <h4><span class="highlight">Kelpie Coin</span> Smart Contract Audit</h4>
          <p>
            Our Kelpie Coin token protocol is being audited by Certik, SGE, Techrate, Solidity, etc. We believe they will not find any high or
            medium security issues in the Smart Contract code. Our Smart Contract code is developed by one of the world's most proficient
            blockchain developers.
          </p>
          <div class="button button-inactive">
            <a href="#">REPORT COMING SOON</a>
          </div>
        </div>
      </div>

      <div class="earn" id="earn">
        <div class="earn__content">
       
          <h3 class="ghost">Earn</h3>
          <h4><span class="highlight">Earn</span> Passive Income</h4>
          <p>
            Gain $KLP every time a transaction is made. Our protocol charges a 5% transaction fee; this means 1% goes into a locked liquidity pool,
            2% is rewarded to our stakeholders, and 2% is donated to a charity supporting Australian Kelpies. No need to trade, simply
            watch your balance increase in real-time. This is called a deflationary currency and will earn up to 80% annual yield percentage -
            exceptionally higher than any traditional savings account.
          </p>
          <a href="https://www.dexlab.space/swap?id=3GQKSGznA6AkyAnhTQorUCwsu811z9hptAvm43Eszcmx" target="_blank" rel="noopener noreferrer" class="button">
            Trade on DexLab
          </a>
        </div>
        <div class="earn__image">
          <img src="./assets/audit.png" alt="Audit Image" />
        </div>
      </div>
    </section>

    <div class="end_bg">
      <section id="network">
        <div class="network">
          <h2>Our Network</h2>
          <div class="underline"></div>
          <div class="network__image--container">
            <a class="network__image" href="https://solana.com/" target="_blank" rel="noopener noreferrer">
              <img src="./assets/sol.svg" alt="Solana Logo" />
            </a>
            <div class="vertical-line"></div>
            <a class="network__image" href="https://www.dexlab.space/" target="_blank" rel="noopener noreferrer">
              <img src="./assets/dexlab.png" alt="DexLab Logo" />
            </a>
          </div>
        </div>
      </section>

      <footer class="footer">
        <p>Copyright © 2021 All Rights Reserved.</p>
      </footer>
    </div>
  </div>
</template>

<script>
import AppNavigation from './components/AppNavigation.vue';
import MobileNav from './components/MobileNav.vue';
import HeroBackgroundAnimation from './components/HeroBackgroundAnimation.vue';

export default {
  name: 'App',
  components: {
    AppNavigation,
    MobileNav,
    HeroBackgroundAnimation,
  },
  data() {
    return {
      showMobileNav: false,
    };
  },
  mounted() {
    const navigationCheckbox = document.querySelector('.navigation__checkbox');

    navigationCheckbox.addEventListener('change', this.toggleScrollLock);
    document.documentElement.style.width = '100vw';
    document.documentElement.style.overflowX = 'hidden';
  },
  beforeUnmount() {
    const navigationCheckbox = document.querySelector('.navigation__checkbox');

    navigationCheckbox.removeEventListener('change', this.toggleScrollLock);
  },
  methods: {
    toggleScrollLock(event) {
      if (event.target.checked) {
        this.lockScroll();
      } else {
        this.unlockScroll();
      }
    },
    toggleMobileNav() {
      this.showMobileNav = !this.showMobileNav;
      if (this.showMobileNav) {
        this.lockScroll();
      } else {
        this.unlockScroll();
      }
    },
    lockScroll() {
      const scrollPosition = window.scrollY;
      const mobileNavSection = document.querySelector('.mobileNav');
      document.body.style.overflow = 'hidden';
      document.body.style.position = 'fixed';
      document.body.style.top = `-${scrollPosition}px`;
      document.documentElement.style.width = '100vw';
      document.body.style.margin = '0';
      mobileNavSection.style.height = '100%';

    },
    unlockScroll() {
      const mobileNavSection = document.querySelector('.mobileNav');
      const scrollPosition = Math.abs(parseInt(document.body.style.top, 10));
      document.body.style.overflow = '';
      document.body.style.position = '';
      document.body.style.top = '';
      document.documentElement.style.overflowX = 'hidden';
      document.documentElement.style.width = '100vw';
      setTimeout(() => {
  mobileNavSection.style.height = '200px';
}, 1000);
      window.scrollTo(0, scrollPosition);
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

#app {
  overflow-x: hidden;
}

html, body {
  background: white;
  font-family: 'Comic Neue', sans-serif;
  scroll-behavior: smooth;
}


body {
  max-width: 1440px;
  margin: auto;
  overflow-x: hidden;
  
}

#token-url {
  text-align: center;
}
.mob, .tablet {
  display: none;
}
#hero .hero {
  display: flex;
  flex-direction: row;
  gap: 0px;
  justify-content: center;
  align-items: center;
  padding: 50px 0;
}

.hero__content {
  color: #8B4513;
  width: 500px;
}

.hero__content--header {
  font-size: 3.5rem;
  font-weight: normal;
  line-height: .75;
  margin: 0;
  font-family: "Fredoka", sans-serif;
width: fit-content;
background: white;
}

.hero__content--subheader {
  font-size: 1rem;
  line-height: 1.5;
  width: 350px;
  margin: 20px 0;
  font-family: 'Times New Roman', Times, serif;
  font-weight: normal;
  background: white;
}

.hero__content--buttonGroup {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.hero__button {
  width: 50%;
  text-align: center;
}

.button {
  background: #FFA500;
  background-size: 400% 400%;
  animation: background-animation 10s ease infinite;
  border-radius: 5px;
  padding: 15px;
  cursor: pointer;
  transition: 0.35s ease-in-out;
  width: fit-content;
  color: white;
  font-weight: normal;
  font-size: 1.25rem;
  text-decoration: none;
  font-family: "Fredoka", sans-serif;

}

.button:hover {
  transform: scale(0.95);
  background-size: 400% 400%;
  animation: background-animation 10s ease infinite;
  border: 1px solid transparent;
}

.button:active {
  transform: scale(0.9);
}

.button-inactive {
  background: #3f3749;
  border: none;
}

.button-inactive:hover {
  transform: scale(0.95);
}

.button-inactive a {
  text-decoration: none;
  color: white;
  cursor:not-allowed;
}

.highlight {
  color: #FFA500;
  font-size: 2rem;
  margin-top: 10px;
}

.hero__image img {
  width: 200px;
  animation: float 10s ease-in-out 0.5s infinite;
}

@media (max-width: 1024px) {
  .hero__content--header {
    font-size: 2.5rem;
    line-height: 1;
  }
  .hero__image img {
    width: 300px;
  }
}

@media (max-width: 768px) {

  .desk {
    display: none;
  }

  .mob, .tablet {
    display: block;
  }
  #hero .hero {
    flex-direction: column-reverse !important;
    margin-top: 125px;
    padding: 0;
  }
  .hero__content {
    margin-bottom: 10px;
    margin-left: 0;
    text-align: center;
    margin-top: 25px;
  }

  .hero__content--header {
    margin: 10px auto auto auto;
  }

  .hero__content--subheader {
    margin: 20px auto;
  }

  .hero__button {
    margin: auto;
  }

  .hero__image img {
    width: 200px;
  }
}

@media (max-width: 425px) {
  .hero__content--header {
    font-size: 2.5rem;
  }
  .hero__content--subheader {
    width: 80%;
    font-size: 1.05rem;
    margin: 25px auto;
  }

  .hero__content {
    width: 100%;
  }
  .hero__button a {
    font-size: 1.05rem;
  }
  .button {
    font-size: 1.1rem;
  }
}

/* About Section */
#about {
  margin-top: 50px;
  color: #8B4513;
}

.about {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 10px 0 10px 0;
  background: url('./assets/about-bg.png'), #fff;
  background-size: 100% auto;
  background-repeat: no-repeat;
  background-position: center;
}

.about__header {
  display: flex;
  align-items: center;
  text-align: center;
  font-weight: lighter;
  font-size: 1.75rem;
  font-family: "Fredoka", sans-serif;

}

.about__header--img img {
  max-width: 50px;
  padding-right: 25px;
}

.about__content {
  font-size: 1.2rem;
  line-height: 2;
  margin-bottom: 25px;
  text-align: left;
  font-size: 1rem;
}

.about__content p {
  width: 70%;
  margin: auto;
}

@media (max-width: 1024px) {
  .about__content p {
    width: 80%;
  }
}

@media (max-width: 768px) {
  .about__content {
    padding: 0 20px;
  }
}

@media (max-width: 426px) {
  .about__header {
    flex-direction: column;
    font-size: 1.5rem;
  }
  .about__header--img img {
    max-width: 100px;
  }

  .about__header h2 {
    margin-top: 0;
  }
  .about__content p {
    font-size: 1rem;
    width: 100%;
  }
  
}

/* Swap Section */
.swap {
  background: linear-gradient(45deg,    
  #8B4513, 
  #B22222, 
  #FFA500, 
  #A0522D, 
  #FFC04D
  );
  background-size: 400% 400%;
  animation: background-animation 10s ease infinite;
  border-radius: 25px;
  color: white;
  width: 80%;
  margin: auto;
  padding: 30px 0;
}

.swap__header {
  display: flex;
  flex-direction: row;
  align-items: center;
  font-size: 1.25rem;
  letter-spacing: 2px;
  word-spacing: 3px;
  justify-content: center;
  gap: 20px;
  font-family: "Fredoka", sans-serif;

}

.swap__header--img img {
  max-width: 75px;
}

.swap__section {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  text-align: center;
  font-size: 1.1rem;
}

.swap__section--item {
}

.item-2 {
  background: #fff;
  width: 150px;
  margin: auto;
  padding: 5px 25px;
  border-radius: 15px;
  color: #8B4513;
  font-size: 1.25rem;
}

@media (max-width: 1024px) {
  .swap {
    padding: 25px 0;
  }
  .swap__section {
    background-position: 200px 0;
  }
}

@media (max-width: 768px) {
  .swap__section {
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr;
    background-position: 0 200px;
  }
}

@media (max-width: 426px) {

  .swap {
    padding: 0;
    width: 100%;
    transform: scale(.95);
  }
  
  .swap__section {
    font-size: 1.1rem;
    background-size: 1500px;
    background-position: bottom;
    display: flex;
        flex-direction: column;
  }

  
}

/* Audit Section */
.audit {
  background: white;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
}

.audit__image img,
.earn__image img {
  max-width: 300px;
}

.audit__content,
.earn__content {
  max-width: 500px;
}

.audit__content h3,
.earn__content h3 {
  font-size: 3rem;
  margin-bottom: -25px;
  opacity: 0.09;
  font-family: "Fredoka", sans-serif;

}

.audit__content h4,
.earn__content h4 {
  font-size: 2rem;
  margin-bottom: 0;
  font-family: "Fredoka", sans-serif;

}

.audit__content p,
.earn__content p {
  font-size: 1rem;
  margin-bottom: 50px;
  line-height: 2;
  width: 90%;
}

.earn {
  background: white;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
}


@media (max-width: 768px) {
  .audit{
    flex-direction: column;
    margin-top: 50px;
  }

  .earn {
    flex-direction: column-reverse;
    margin-top: 50px;
  }
  .audit__image,
  .earn__image {
    justify-content: center;
  }
  .audit .button,
  .earn .button {
    margin: auto;
    display: flex;
  }
  .audit__content h3,
  .earn__content h3,
  .audit__content h4,
  .earn__content h4 {
    margin: auto;
  }

  .audit__content p, .earn__content p {
    width: 100%;
  }
}

@media (max-width: 425px) {
  .audit{
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .earn {
    flex-direction: column-reverse;
    justify-content: center;
    align-items: center;
  }
  .audit__image img,
  .earn__image img {
    max-width: 350px;
  }
}

/* Network Section */
.end_bg {
  color: black;
}

.network {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding-top: 50px;
  text-align: center;
}

.network h2 {
  font-size: 2rem;
  color: #8B4513;
  font-weight: bold;
  font-family: "Fredoka", sans-serif;

}

.network__image--container {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
  margin-top: 20px;
  width: 100%;
}

.network__image img {
  max-width: 100px;
}

.vertical-line {
  height: 200px;
  width: 1px;
  background: #fada00;
}

.footer {
  text-align: center;
  padding: 0 0 20px;
  color: rgba(255, 255, 255, 0.5);
}


@media (max-width: 768px) {
  .network__image img {
    max-width: 100px;
  }
  .vertical-line {
    height: 100px;
  }
}

@media (max-width: 426px) {
  .network__image--container {
    flex-direction: column;
    margin-top: 50px;
  }
  .vertical-line {
    height: 1px;
    width: 300px;
    margin: 50px 0;
  }

  .swap {
    width: 100% !important;
    padding: 25px 0px;
  }


  .audit__content, .earn__content {
    padding: 0 20px;
  }
}
</style>
