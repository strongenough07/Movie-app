<template>
  <div class="home">
    <Hero />
  </div>
</template>

<script>
import axios from "axios"
export default {
  data() {
    return {
      movie: [],

    }
  },
  methods: {
    async getMovies() {
      const data = axios.get(`https://api.themoviedb.org/3/movie/now_playing?api_key=ef8e564871e2670bf18156e3c9186160&language=en-US&page=1`)
      const result = await data
      console.log(result);
    }
  }
}
</script>
