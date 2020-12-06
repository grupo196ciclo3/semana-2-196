<template>
  <div class="row mt-md-5 mt-sm-5 mt-xs-5">
    <div
      class="col-lg-6 col-xs-12 bg-success border p-3 rounded"
      v-for="(item, index) of movies"
      :key="index">
      <div class="d-flex justify-content-around align-items-center">
        <div class="p-3">
          <img
            class="img-fluid"
            :src="item.Poster"
            alt="imagen de la pelicula"
          />
        </div>
        <div class="p-2">
          <h4>{{ item.Title }}</h4>
          <h5>{{ item.Type }}</h5>
          <h5>{{ item.Year }}</h5>
          <a
            :href="'https://www.imdb.com/title/' + item.imdbID"
            class="btn btn-info" target="_blank"
            >Go To Watch Movie >></a
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "ComponenteNoticias",
  data() {
    return {
      movies: null,
    };
  },
  mounted() {
    axios
      .get("http://www.omdbapi.com/?s=john&type=movie&apikey=d0d830ce")
      .then((response) => {
        (this.movies = response.data.Search.slice(0,4))
        console.log(this.movies);
      });
  },
};
</script>