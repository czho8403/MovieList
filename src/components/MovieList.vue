<template>
  <div>
    <h2>Movie List</h2>
    <ul>
      <li v-for="movie in movies" :key="movie.imdbID">
        <div>{{ movie.Title }}</div>
        <div>{{ movie.Year }}</div>
        <div>{{ movie.Type }}</div>
        <div>{{ movie.Poster }}</div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    movies: Array
  }
}
</script>
