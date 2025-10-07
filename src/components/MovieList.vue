<template>
  <v-card class="pa-4" elevation="3">
    <h3 class="text-h5 mb-4 text-center">🎬 Resultados</h3>

    <v-row>
      <v-col
        v-for="movie in movies"
        :key="movie.imdbID"
        cols="12" sm="6" md="4"
      >
        <v-card
          class="hoverable"
          elevation="2"
          @click="selectMovie(movie.imdbID)"
        >
          <v-img
            :src="movie.Poster !== 'N/A' ? movie.Poster : 'https://via.placeholder.com/300x450?text=Sin+Imagen'"
            height="300px"
            cover
          />
          <v-card-title class="text-center">{{ movie.Title }}</v-card-title>
          <v-card-subtitle class="text-center">{{ movie.Year }}</v-card-subtitle>
        </v-card>
      </v-col>
    </v-row>
  </v-card>
</template>

<script setup>
const props = defineProps({
  movies: {
    type: Array,
    required: true
  }
})

const emit = defineEmits(['select-movie'])

const selectMovie = (id) => {
  emit('select-movie', id)
}
</script>

<style scoped>
.hoverable:hover {
  cursor: pointer;
  transform: scale(1.02);
  transition: all 0.2s ease;
}
</style>