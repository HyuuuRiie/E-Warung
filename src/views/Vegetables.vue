<template>
  <div class>
    <Navbar />
    <div class="container">
      <div class="row mt-4">
        <div class="col">
          <h2>List <strong>Food</strong></h2>
        </div>
      </div>
      <div class="row-mt-3">
        <div class="col">
          <div class="input-group mb-3">
            <input
              v-model="search"
              type="text"
              class="form-control"
              placeholder="Find Best Foods"
              aria-label="Cari"
              aria-describedby="basic-addon1"
              @keyup="searchVegetable"
            />
            <span class="input-group-text" id="basic-addon1"
              ><b-icon-search></b-icon-search
            ></span>
          </div>
        </div>
      </div>
      <div class="row mb-4">
        <div
          class="col-md-4 mt-4"
          v-for="product in products"
          :key="product.id"
        >
          <CardProduct :product="product" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import CardProduct from "@/components/CardProduct.vue";
import axios from "axios";

export default {
  name: "Vegetables",
  components: {
    Navbar,
    CardProduct,
  },
  data() {
    return {
      products: [],
      search: '',
    };
  },
  // data yang diambil dari json dimasukkan dalam product
  methods: {
    setProduct(data) {
      this.products = data;
    },
    searchVegetable() {
      axios
        .get("http://localhost:3000/products?q=" + this.search)
        .then((response) =>
          // handle success
          this.setProduct(response.data)
        )
        .catch((error) => console.log(error));
    },
  },
  mounted() {
    axios
      .get("http://localhost:3000/products")
      .then((response) =>
        // handle success
        this.setProduct(response.data)
      )
      .catch((error) => console.log(error));
  },
};
</script>

<style>
</style>