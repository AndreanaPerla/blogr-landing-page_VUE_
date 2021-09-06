<template>
  <footer class="footer">
    <h1 class="footer-logo">Blogr</h1>
    <div class="product">
      <p class="footer-title">Product</p>
      <a href="">Overview</a>
      <a href="">Pricing</a>
      <a href="">Marketplace</a>
      <a href="">Features</a>
      <a href="">Integrations</a>
    </div>
    <div class="company">
      <p class="footer-title">Company</p>
      <a href="">About</a>
      <a href="">Team</a>
      <a href="">Blog</a>
      <a href="">Careers</a>
    </div>
    <div class="connect">
      <p class="footer-title">Connect</p>
      <a href="">Contact</a>
      <a href="">Newsletter</a>
      <a href="">LinkedIn</a>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped>
.footer {
  background-color: hsl(240, 10%, 16%);
  color: hsl(240, 2%, 79%);
  border-radius: 0 6rem 0 0;
  display: flex;
  justify-content: space-between;
  padding: 6.5% 20.5% 4.5% 10.5%;
}

.footer h1 {
  font-weight: 600;
  font-size: 2.5vw;
}

.product,
.company,
.connect {
  display: flex;
  flex-direction: column;
}

.footer a {
  line-height: 2rem;
  text-decoration: none;
  color: hsl(240, 2%, 79%);
}

.footer a:hover {
  text-decoration: underline;
}

.footer-title {
  font-weight: bold;
  padding-bottom: 30%;
}

@media (max-width: 800px) {
  .footer {
    padding: 8% 20.5% 4.5% 10.5%;
  }

  .footer h1 {
    font-size: 3vw;
  }
}

@media (max-width: 480px) {
  .footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: unset;
    padding: 10% 0 4.5% 0;
    text-align: center;
  }

  .footer h1 {
    font-size: 6vw;
  }

  .product,
  .company,
  .connect {
    padding-bottom: 7%;
  }

  .product {
    padding-top: 10%;
  }
}
</style>
