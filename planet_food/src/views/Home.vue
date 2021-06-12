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

      <div class="row mb-4">
        <div
          class="col-md-4 mt-4"
          v-for="product in products"
          :key="product.id"
        >
          <card-product :product="product" />
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
import axios from 'axios';

export default {
  name: 'Home',
  components: {
    Navbar,
    Hero,
    CardProduct,
  },
  data() {
    return {
      products: [],
    };
  },
  methods: {
    setProduct(data) {
      this.products = data;
    },
  },
  mounted() {
    axios
      .get('http://localhost:3000/best-products')
      .then((response) =>
        // handle success
        this.setProduct(response.data)
      )
      .catch((error) =>
        // handle error
        console.log(error)
      );
  },
};
</script>
