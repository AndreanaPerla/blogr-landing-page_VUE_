<template>
  <div class="header-container">
    <nav class="nav">
      <div class="left-nav">
        <h1 class="logo">Blogr</h1>
        <div class="links">
          <div class="product-menu">
            <a href="" class="menu-link" @click.prevent="openCloseA"
              >Product
              <span><img src="../images/icon-arrow-light.svg" alt=""/></span
            ></a>
            <div class="menu-links-container" v-if="isOpenA">
              <!-- :class="{ '.menu-links-container--isOpen': isOpenA }" -->
              <div class="menu-links">
                <a href="">Overview</a>
                <a href="">Pricing</a>
                <a href="">Marketplace</a>
                <a href="">Features</a>
                <a href="">Integrations</a>
              </div>
            </div>
          </div>
          <div class="company-menu">
            <a href="" class="menu-link" @click.prevent="openCloseB"
              >Company
              <span><img src="../images/icon-arrow-light.svg" alt=""/></span
            ></a>
            <div class="menu-links-container" v-if="isOpenB">
              <!-- :class="{ '.menu-links-container--isOpen': isOpenB }" -->
              <div class="menu-links">
                <a href="">About</a>
                <a href="">Team</a>
                <a href="">Blog</a>
                <a href="">Careers</a>
              </div>
            </div>
          </div>
          <div class="connect-menu">
            <a href="" class="menu-link" @click.prevent="openCloseC"
              >Connect
              <span><img src="../images/icon-arrow-light.svg" alt=""/></span
            ></a>
            <div class="menu-links-container" v-if="isOpenC">
              <!-- :class="{ '.menu-links-container--isOpen': isOpenC }" -->
              <div class="menu-links">
                <a href="">Contact</a>
                <a href="">Newsletter</a>
                <a href="">LinkedIn</a>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="right-nav">
        <a href="" class="login">Login</a>
        <a href="" class="sign">Sign Up</a>
        <a href="" class="hamburger-menu" @click.prevent="openMobileMenu"
          ><img src="../images/icon-hamburger.svg" alt="hamburger-menu"
        /></a>
        <div class="mobile-menu" v-if="isOpenMobile">
          <div class="product-mobile-menu">
            <a href="" class="mobile-menu-link" @click.prevent="openMobileA"
              >Product
              <span><img src="../images/icon-arrow-dark.svg" alt=""/></span
            ></a>
            <div class="mobile-links-container" v-if="isOpenMobileA">
              <div class="mobile-links">
                <a href="">Overview</a>
                <a href="">Pricing</a>
                <a href="">Marketplace</a>
                <a href="">Features</a>
                <a href="">Integrations</a>
              </div>
            </div>
          </div>
          <div class="company-mobile-menu">
            <a href="" class="mobile-menu-link" @click.prevent="openMobileB"
              >Company
              <span><img src="../images/icon-arrow-dark.svg" alt=""/></span
            ></a>
            <div class="mobile-links-container" v-if="isOpenMobileB">
              <div class="mobile-links">
                <a href="">About</a>
                <a href="">Team</a>
                <a href="">Blog</a>
                <a href="">Careers</a>
              </div>
            </div>
          </div>
          <div class="connect-mobile-menu">
            <a href="" class="mobile-menu-link" @click.prevent="openMobileC"
              >Connect
              <span><img src="../images/icon-arrow-dark.svg" alt=""/></span
            ></a>
            <div class="mobile-links-container" v-if="isOpenMobileC">
              <div class="mobile-links">
                <a href="">Contact</a>
                <a href="">Newsletter</a>
                <a href="">LinkedIn</a>
              </div>
            </div>
          </div>
          <hr />
          <div class="mobile-login-sign">
            <a href="" class="mobile-login">Login</a>
            <a href="" class="mobile-sign">Sign Up</a>
          </div>
        </div>
      </div>
    </nav>
    <header class="header">
      <h1 class="title">A modern publishing platform</h1>
      <h4 class="subtitle">Grow your audience and build your online brand</h4>
      <div class="cta">
        <a type="button" class="start">Start for Free</a>
        <a type="button" class="learn">Learn More</a>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      isOpenA: false,
      isOpenB: false,
      isOpenC: false,
      isOpenMobile: false,
      isOpenMobileA: false,
      isOpenMobileB: false,
      isOpenMobileC: false,
    };
  },
  methods: {
    openCloseA() {
      this.isOpenA = !this.isOpenA;
    },
    openCloseB() {
      this.isOpenB = !this.isOpenB;
    },
    openCloseC() {
      this.isOpenC = !this.isOpenC;
    },
    openMobileMenu() {
      this.isOpenMobile = !this.isOpenMobile;
    },
    openMobileA() {
      this.isOpenMobileA = !this.isOpenMobileA;
    },
    openMobileB() {
      this.isOpenMobileB = !this.isOpenMobileB;
    },
    openMobileC() {
      this.isOpenMobileC = !this.isOpenMobileC;
    },
  },
};
</script>

<style scoped>
.header-container {
  width: 100%;
  height: 70vh;
  background: url("../images/bg-pattern-intro.svg"),
    linear-gradient(to right, hsl(13, 100%, 72%), hsl(353, 100%, 62%));
  background-position: 28.25% 52%, 0% 0%;
  background-size: 240%, 100%;
  background-repeat: no-repeat, no-repeat;
  border-radius: 0 0 0 6rem;
  color: white;
}

.nav {
  display: flex;
  align-items: center;
  padding: 4% 11% 0 11%;
  position: relative;
}

.left-nav {
  display: flex;
  flex: 2;
  align-items: center;
}

.logo {
  font-weight: 600;
  font-size: 2.5vw;
  padding-right: 7%;
}

.links {
  display: flex;
}

.menu-link {
  display: flex;
  text-decoration: none;
  color: white;
}

.product-menu,
.company-menu,
.connect-menu {
  padding-right: 10%;
}

.menu-links-container {
  display: block;
  position: absolute;
  top: 100%;
  animation: 0.25s fadeIn ease;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

.menu-links {
  display: flex;
  flex-direction: column;
  background-color: white;
  padding: 1.75vw 3.35vw 1.75vw 1.35vw;
  border-radius: 0.5rem;
  line-height: 1.75rem;
}

.menu-links a {
  text-decoration: none;
  color: hsl(208, 49%, 24%);
}

.menu-links a:hover {
  font-weight: bold;
}

.menu-link span {
  padding-left: 5%;
}

.right-nav {
  flex: 1;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  font-weight: bold;
}

.login {
  text-decoration: none;
  color: white;
  padding-right: 6%;
}

.sign {
  text-decoration: none;
  background-color: white;
  padding: 2.75% 8.5%;
  border-radius: 2rem;
  color: hsl(356, 100%, 66%);
}

.menu-link:hover,
.login:hover {
  text-decoration: underline;
}

.sign:hover,
.start:hover {
  background-color: hsl(355, 100%, 74%);
  color: white;
}

.header {
  min-height: 58vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.title {
  font-size: 4vw;
}

.subtitle {
  font-size: 1.4vw;
  letter-spacing: 0.025rem;
  font-weight: 300;
  padding-top: 2.25%;
  padding-bottom: 3.25%;
}

.cta {
  width: 25%;
  display: flex;
  justify-content: space-evenly;
}

.cta a {
  border-radius: 2rem;
  font-weight: bold;
  cursor: pointer;
}

.start {
  border: none;
  background-color: white;
  color: hsl(356, 100%, 66%);
  padding: 3.25% 8.75%;
}

.learn {
  border: 1px solid white;
  background-color: transparent;
  color: white;
  padding: 3% 8.75%;
}

.learn:hover {
  background-color: white;
  color: hsl(356, 100%, 66%);
}

.hamburger-menu {
  display: none;
}

.mobile-menu {
  display: none;
}

@media (max-width: 800px) {
  .logo {
    font-size: 3vw;
  }

  .title {
    font-size: 4.5vw;
  }

  .subtitle {
    font-size: 1.9vw;
  }

  .cta {
    width: 40%;
  }
}

@media (max-width: 480px) {
  .nav {
    padding: 11% 5% 0 5%;
    position: relative;
  }

  .logo {
    font-size: 6vw;
  }

  .links,
  .login,
  .sign {
    display: none;
  }

  .hamburger-menu {
    display: block;
  }

  .hamburger-menu:hover {
    transform: scale(1.1);
  }

  .mobile-menu {
    z-index: 99;
    position: absolute;
    top: 110%;
    right: 10%;
    width: 80%;
    border-radius: 0.5rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: white;
    padding: 5% 0;
    box-shadow: 0 0 30px rgba(0, 0, 0, 0.25);
    animation: 0.25s fadeInMobile ease;
  }

  @keyframes fadeInMobile {
    0% {
      opacity: 0;
    }
    100% {
      opacity: 1;
    }
  }

  .product-mobile-menu,
  .company-mobile-menu,
  .connect-mobile-menu {
    padding-bottom: 3%;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .mobile-menu-link {
    text-decoration: none;
    color: hsl(208, 49%, 24%);
    font-size: 3vw;
  }

  .mobile-menu-link:hover {
    text-decoration: underline;
  }

  hr {
    width: 80%;
    border: 0;
    border-top: 1px solid rgb(218, 218, 218);
    padding-bottom: 3%;
  }

  .mobile-links-container {
    width: 90%;
    animation: 0.25s fadeInMobile ease;
  }

  .mobile-links {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: rgb(236, 236, 236);
    border-radius: 0.25rem;
    padding: 4% 0 1% 0;
  }

  .mobile-links a {
    text-decoration: none;
    color: hsl(207, 13%, 34%);
    padding-bottom: 3%;
  }

  .mobile-login-sign {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 80%;
  }

  .mobile-login-sign a {
    text-decoration: none;
    font-size: 3vw;
  }

  .mobile-login {
    color: hsl(208, 49%, 24%);
    padding-bottom: 3%;
  }

  .mobile-login:hover {
    text-decoration: underline;
  }

  .mobile-sign {
    background-color: hsl(356, 100%, 66%);
    padding: 2.75% 8.5%;
    border-radius: 2rem;
    color: white;
  }

  .mobile-sign:hover {
    background: hsl(355, 100%, 74%);
  }

  .title {
    width: 75%;
    font-size: 8vw;
    text-align: center;
  }

  .subtitle {
    width: 75%;
    font-size: 4vw;
    text-align: center;
  }

  .cta {
    width: 75%;
  }
}
</style>
