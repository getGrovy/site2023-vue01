<template>
  <ContTitle title="movies" />
  <MovieSlider />
  <MoveSearch />
  <MovieTag />
  <MovieCont :movies="movies" />
</template>
<script>
import ContTitle from "@/components/layout/ContTitle.vue";
import MoveSearch from "@/components/movie/MoveSearch.vue";
import MovieSlider from "@/components/movie/MovieSlider.vue";
import MovieTag from "@/components/movie/MovieTag.vue";
import MovieCont from "@/components/movie/MovieCont.vue";
import { ref } from "vue";

export default {
  components: {
    ContTitle,
    MovieSlider,
    MoveSearch,
    MovieTag,
    MovieCont,
  },

  setup() {
    //setup()으로 넣어야함
    const movies = ref([]);
    const searchs = ref([]);
    const search = ref("marvel");
    const TopMovies = async () => {
      await fetch(
        `https://api.themoviedb.org/3/movie/popular?api_key=3db0ef208fc69d8508e6827ad1312b12&query=${search.value}`
      )
        .then((response) => response.json())
        .then((result) => {
          // console.log(result);
          movies.value = result.results;
          searchs.value = result.results;
        })
        .catch((error) => console.log("error", error));
    };
    TopMovies();
    return {
      TopMovies,
      movies,
      searchs,
    };
  },
};
</script>
