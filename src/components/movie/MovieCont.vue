<template>
  <div className="movie__cont container">
    <ul>
      <li v-for="(movie, index) in movies" :key="index">
        <a :href="`https://www.themoviedb.org/movie/${movie.id}`">
          <img
            :src="`https://image.tmdb.org/t/p/w500/${movie.poster_path}`"
            :alt="`${movie.title}`"
          />
          <em>
            <span class="title">{{ movie.title }}</span>
            <span class="start">{{ movie.vote_average }}</span>
          </em>
        </a>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  props: {
    movies: {
      type: Array,
      required: true,
    },
  },
};
</script>
