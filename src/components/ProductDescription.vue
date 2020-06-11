<template>
  <div>
    <b-jumbotron>
      <b-container fluid>
        <b-row>
          <b-col sm="12">
            <h2>{{information[0] ['name']}}</h2>
          </b-col>
          <b-col style="margin-top:20px" sm="12">
            <h3>Price: Rs {{information [0]['price']}}</h3>
          </b-col>
          <b-col style="margin-top:20px" sm="12">
            <ul style="text-align:left;">
              <li v-for="(data, index) in information[0]['details']" :key="index">{{data}}</li>
            </ul>
          </b-col>
          <b-col style="margin-top:20px" sm="12">
            <b-button variant="outline-primary">Add to Cart</b-button>
            <b-button variant="outline-primary">Buy Now</b-button>
          </b-col>
        </b-row>
      </b-container>
    </b-jumbotron>
  </div>
</template>

<script>
export default {
  props: { information: Array },
  data: function() {
    return {};
  },
  mounted: function() {}
};
</script>

<style>
.btn {
  margin: 0px 5px;
}
</style>