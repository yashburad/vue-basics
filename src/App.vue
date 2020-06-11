<template>
  <div id="app">
    <Header />
    <b-container fluid class="bv-example-row">
      <b-row>
        <b-col sm="6">
          <Product :images="data[0]['images']" />
        </b-col>
        <b-col sm="6">
          <ProductDescription :information="data" />
        </b-col>
      </b-row>
      <b-row>
        <b-col sm="12" style="overflow-y:auto; margin:20px;">
          <h3>Technical Specifications</h3>
        </b-col>
        <b-col sm="12" style="overflow-y:auto;">
          <b-table stacked striped bordered hover :items="data[0]['technical']"></b-table>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Product from "./components/Product.vue";
import ProductDescription from "./components/ProductDescription.vue";
import data from "@/data/iphone.js";

export default {
  name: "App",
  components: {
    Header,
    Product,
    ProductDescription
  },
  data() {
    return {
      data
      // images
    };
  },
  mounted: function() {
    // this.images = data[0]["images"];
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}

.table.b-table.b-table-stacked > tbody > tr > [data-label]::before {
  text-align: center !important;
  border-right: 1px solid;
}
</style>
