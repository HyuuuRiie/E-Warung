<template>
  <div class="hero">
    <!-- Desktop -->
    <div class="d-none d-md-block">
      <div class="row mt-4">
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2><strong>Home Made Food, </strong><br />in Your Gadget</h2>
              <p>
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. A,
                sapiente earum. Laudantium ullam dolor veniam totam nostrum,
                deleniti molestiae iure rem consequatur temporibus laboriosam
                accusamus, sapiente voluptate eaque dolores at.
              </p>
              <router-link class="btn btn-lg btn-outline-success" to="/vegetables">Order Now</router-link>
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <img src="../assets/images/hero.png" alt="Ini Gambar" width="100%" />
        </div>
      </div>
    </div>
    <!-- mobile -->
    <div class="d-sm-block d-md-none">
      <div class="row mt-4">
        <div class="col-md-6 mb-3">
          <img src="../assets/images/hero.png" alt="Ini Gambar" width="100%" />
        </div>
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2><strong>Fresh Vegetables, </strong><br />in Your Gadget</h2>
              <p>
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. A,
                sapiente earum. Laudantium ullam dolor veniam totam nostrum,
                deleniti molestiae iure rem consequatur temporibus laboriosam
                accusamus, sapiente voluptate eaque dolores at.
              </p>
              <button class="btn btn-lg btn-outline-success">Order Now</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Hero",
};
</script>

<style>
</style>