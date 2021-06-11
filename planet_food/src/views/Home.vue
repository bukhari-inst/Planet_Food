<template>
  <div class="home">
    <navbar />
    <div class="container">
      <Hero />
      <row class="row mt-4">
        <div class="col">
          <h2>Best <Strong>Foods</Strong></h2>
        </div>
        <div class="col">
          <router-link to="/foods" class="btn btn-success float-right"
            ><b-icon-eye></b-icon-eye> See All</router-link
          >
        </div>
      </row>

      <div class="row mb-3">
        <div class="col-md-4 mt-4">
          <card-product />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue';
import Hero from '@/components/Hero.vue';
import CardProduct from '@/components/CardProduct.vue';

export default {
  name: 'Home',
  components: {
    Navbar,
    Hero,
    CardProduct,
  },
};
</script>
