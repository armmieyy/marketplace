<template>
  <div class="row text-light">
    <div class="col-sm" />
    <div class="col-sm">
      <input v-model="textSearch" type="text" placeholder="ชื่อสินค้า" class="red--text">
      <v-btn
        squared
        variant="outline-danger"
        @click="searchData()"
      >
        Search
      </v-btn>
      <br>
      <br>
      <br>
      <v-card
        class="mx-auto"
        max-width="400"
      >
        <v-img
          class="white--text align-end"
          height="350px"
          src="https://www.thailand.intel.com/content/dam/products/hero/foreground/badge-9th-gen-core-i9-1x1.png.rendition.intel.web.225.225.png"
        >
          <v-card-title>Top 10 benchmark processor</v-card-title>
        </v-img>

        <v-card-subtitle class="pb-0">
          Number 10
        </v-card-subtitle>

        <v-card-text class="text--primary">
          <div>Intel Core I9 9900K</div>
        </v-card-text>

        <v-card-actions>
          <v-btn
            color="orange"
            text
          >
            Share
          </v-btn>

          <v-btn
            color="orange"
            text
          >
            Explore
          </v-btn>
        </v-card-actions>
      </v-card>
      <li
        v-for="data in store"
        :key="data.mal_id"
      >
        <nuxt-link :to="{ name: 'product-id', params: { data: data } }">
          {{ data.title }}
        </nuxt-link>
      </li>
      <br>
      <br>
    </div>

    <div class="col-sm" />
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data () {
    return {
      animeData: null,
      textSearch: '',
      perPage: 9,
      currentPage: 1,
      run: false
    }
  }
}
</script>

<style>
.card {
  background-color: rgb(45, 110, 175);
}
.pagination {
  justify-content: center;
}
</style>
