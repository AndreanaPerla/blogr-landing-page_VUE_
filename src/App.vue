<template>
  <Header />
  <DesignForFuture />
  <Footer />
</template>

<script>
import Header from "./components/Header.vue";
import DesignForFuture from "./components/DesignForFuture.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    DesignForFuture,
    Footer,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Overpass:wght@300;600&display=swap");
/* font-family: 'Overpass', sans-serif; */
@import url("https://fonts.googleapis.com/css2?family=Ubuntu:wght@400;500;700&display=swap");
/* font-family: 'Ubuntu', sans-serif; */

* {
  margin: 0 !important;
  font-size: 1.2vw;
  font-family: "Overpass", sans-serif;
}

@media (max-width: 800px) {
  * {
    font-size: 1.75vw;
  }
}

@media (max-width: 480px) {
  * {
    font-size: 2.75vw;
  }
}

/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
