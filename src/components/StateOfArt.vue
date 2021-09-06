<template>
  <div class="stateOfArt-container">
    <div class="stateOfArt-img">
      <img src="../images/illustration-phones.svg" alt="illustration-phones" />
    </div>
    <div class="stateOfArt-text">
      <h4>State of the Art Infrastructure</h4>
      <p>
        With reliability and speed in mind, worldwide data center provide the
        backbone for ultra-fast connectivity. This ensures your site will load
        instantly, no matter where your readers are, keeping your site
        competitive.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "StateOfArt",
};
</script>

<style scoped>
.stateOfArt-container {
  display: flex;
  justify-content: flex-end;
  background-color: hsl(237, 23%, 32%);
  background: url("../images/bg-pattern-circles.svg"),
    linear-gradient(to right, hsl(237, 17%, 21%), hsl(237, 23%, 32%));
  background-position: -49% 85%, 0% 0%;
  background-size: 70%, 100%;
  background-repeat: no-repeat, no-repeat;
  border-radius: 0 6rem 0 6rem;
  position: relative;
  padding-right: 10.5%;
}

.stateOfArt-img {
  position: absolute;
  top: -15%;
  left: 9%;
}

.stateOfArt-img img {
  width: 38.5vw;
}

.stateOfArt-text {
  width: 43.5%;
  color: white;
  letter-spacing: 0.025rem;
  padding-top: 9%;
  padding-bottom: 8%;
}

.stateOfArt-text h4 {
  font-size: 2.5vw;
  padding-bottom: 5.25%;
}

.stateOfArt-text p {
  line-height: 1.75rem;
}

@media (max-width: 800px) {
  .stateOfArt-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: unset;
    padding-right: 0;
  }

  .stateOfArt-img {
    position: absolute;
    top: -45%;
    left: 30%;
  }

  .stateOfArt-text {
    width: 80%;
    padding-top: 20%;
    padding-bottom: 8%;
    text-align: center;
  }

  .stateOfArt-text h4 {
    font-size: 3vw;
    padding-bottom: 5.25%;
  }
}

@media (max-width: 480px) {
  .stateOfArt-text h4 {
    font-size: 4vw;
    padding-bottom: 5.25%;
  }

  .stateOfArt-img img {
    width: 70vw;
  }

  .stateOfArt-img {
    position: absolute;
    top: -45%;
    left: 13.5%;
  }

  .stateOfArt-text {
    width: 80%;
    padding-top: 40%;
    padding-bottom: 8%;
    text-align: center;
  }
}
</style>
