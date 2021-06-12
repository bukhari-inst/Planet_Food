<template>
  <div class="hero">
    <!-- Dekstop -->
    <div class="d-none d-md-block">
      <div class="row mt-4 ">
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong>Delicious Food Menu, </strong> <br />
                in Your Gadget
              </h2>
              <p>Come on, choose and order your favorite food</p>
              <router-link class="btn btn-lg btn-success" to="foods">
                <b-icon-arrow-right></b-icon-arrow-right> Order
              </router-link>
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <img src="../assets/images/hero.png" width="100%" alt="" />
        </div>
      </div>
    </div>

    <!-- Mobile -->
    <d-sm-block class="d-md-none">
      <div class="row mt-4 ">
        <div class="col-md-6 mb-2">
          <img src="../assets/images/hero.png" width="100%" alt="" />
        </div>
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong>Delicious Food Menu, </strong> <br />
                in Your Gadget
              </h2>
              <p>Come on, choose and order your favorite food</p>
              <button class="btn btn-lg btn-success">
                <b-icon-arrow-right></b-icon-arrow-right> Order
              </button>
            </div>
          </div>
        </div>
      </div>
    </d-sm-block>
  </div>
</template>

<script>
export default {
  name: 'Hero',
};
</script>

<style></style>
