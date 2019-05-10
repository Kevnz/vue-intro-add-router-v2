<template>
  <div class="about">
    <ShoppingCart v-bind:cart="cart"/>
    <div id="app">
      <h1>
        <img class="logo" alt="Vue logo" src="../assets/logo.png">The Vue.js Shop
      </h1>
      <div id="nav">
        <router-link to="/">Home</router-link>
        <router-link to="/checkout">Checkout</router-link>
        <router-link to="/about">About</router-link>
      </div>
      <div>This is an example application used to demonstrate using Vue.js</div>
      <div>This is the second iteration that adds the vue router and a checkout page</div>
    </div>
    <a
      href="https://github.com/Kevnz/vue-intro-third-add-router"
      class="github-corner"
      aria-label="Open GitHub project"
    >
      <svg
        width="80"
        height="80"
        viewBox="0 0 250 250"
        style="position: absolute; top: 0px; fill: rgb(255, 255, 255); left: 0px;"
      >
        <path class="octo-banner" d="M250 0L135 115h-15l-12 27L0 250V0z" fill="#151513"></path>
        <path
          class="octo-arm"
          d="M122 109c15-9 9-19 9-19-3-7-2-11-2-11 1-7-3-2-3-2-4 5-2 11-2 11 3 10-5 15-9 16"
          style="transform-origin: 120px 144px 0px;"
        ></path>
        <path
          class="octo-body"
          d="M135 115s-4 2-5 0l-14-14c-3-2-6-3-8-3 8-11 15-24-2-41-5-5-10-7-16-7-1-2-3-7-12-11 0 0-5 3-7 16-4 2-8 5-12 9s-7 8-9 12c-14 4-17 9-17 9 4 8 9 11 11 11 0 6 2 11 7 16 16 16 30 10 41 2 0 3 1 7 5 11l12 11c1 2-1 6-1 6z"
        ></path>
      </svg>
    </a>
  </div>
</template>
<script>
import ShoppingCart from "@/components/ShoppingCart.vue";

export default {
  name: "about",
  components: {
    ShoppingCart
  },
  data() {
    return {
      products: window.cart || [],
      cart: window.cart || []
    };
  }
};
</script>