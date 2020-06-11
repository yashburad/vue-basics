<template>
  <div>
    <b-container fluid>
      <b-row>
        <b-col sm="2">
          <ul>
            <img
              class="image"
              v-for="(image,index) in images"
              @click="select(index)"
              :key="index"
              :src="image"
            />
          </ul>
        </b-col>

        <b-col sm="10">
          <img
            class="image1"
            style="height:500px; width:auto;"
            :key="index"
            :src="images[selectedIndex]"
          />
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  props: { images: Array },
  data: function() {
    return {
      selectedIndex: 0
    };
  },
  methods: {
    focus(index1) {
      this.selectedIndex = index1;
    },
    select(index1) {
      this.selectedIndex = index1;
    }
  }
};
</script>

<style>
.image {
  margin-bottom: 20px;
  width: 50px;
  cursor: pointer;
}

@media screen and (max-width: 720px) {
  .image1 {
    width: 300px !important;
    height: auto !important;
  }
  ul {
    margin-top: 20px !important;
    padding-left: 0px !important;
  }
}
</style>