<template>
  <div class="containr">
      <input class="key mr-3" type="text" v-model="keyword" />
      <button type="rounded" class="btn btn-secondary" @click="searchData()" > SEARCH MUSIC </button>
      <!-- {{resultData}} -->
    <div><br>
  <div class="containr">
      <b-card-group columns>
        <b-card v-for="data in resultData"
          :key="data.trackId"
          :title="data.trackName"
          :img-src="data.artworkUrl60"
          img-alt="Image"
          img-top
          tag="article"
          style="max-width: 20rem"
          class="mb-2"
        >
        
          <audio controls>
            <source :src="data.previewUrl" type="audio/mpeg" />
          </audio>
          <b-button :href="data.trackViewUrl" variant="primary"
            ></b-button >
        </b-card>
        </b-card-group>
      
   </div> 
  </div>
  
  </div>
</template>


<script>
import Axios from "axios";
export default {
  data() {
    return {
      resultData: null,
      keyword: "",
    };
  },

  methods: {
    searchData() {
      console.log("searchData");
      Axios.get("https://itunes.apple.com/search?term=" + this.keyword + "")
        .then((response) => {
          this.resultData = response.data.results;
        })
        .catch((err) => {
          console.log(err);
        });
    },
  },
};
</script>


<style>
body{
  background-color: rgb(236, 234, 234);
}

</style>