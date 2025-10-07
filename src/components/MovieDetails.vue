<template>
  <v-dialog v-model="dialog" max-width="800px" color="red" persistent >
    <v-card>
      <v-toolbar color="#0C0F6B" dark>
        <v-toolbar-title>{{ movie.Title }}</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn icon @click="closeDetails">
          <v-icon>mdi-close</v-icon>
        </v-btn>
      </v-toolbar>

      <v-card-text>
        <v-container>
          <v-row>
            <v-col cols="12" md="4">
              <v-img
                :src="movie.Poster !== 'N/A' ? movie.Poster : 'https://via.placeholder.com/300x450?text=Sin+Imagen'"
                height="300px"
                cover
              />
            </v-col>

            <v-col cols="12" md="8">
              <p><strong>Año:</strong> {{ movie.Year }}</p>
              <br>
              <p><strong>Género:</strong> {{ movie.Genre }}</p>
              <br>
              <p><strong>Director:</strong> {{ movie.Director }}</p>
              <br>
              <p><strong>Actores:</strong> {{ movie.Actors }}</p>
              <br>
              <p><strong>Calificación IMDB:</strong> {{ movie.imdbRating }}</p>
              <br>
              <p><strong>Sinopsis:</strong> {{ movie.Plot }}</p>
            </v-col>
          </v-row>
        </v-container>
      </v-card-text>
    </v-card>
  </v-dialog>
</template>

<script setup>
import { ref, watch } from 'vue'

const props = defineProps({
  movie: {
    type: Object,
    required: true
  }
})

const emit = defineEmits(['close-details'])
const dialog = ref(true)

const closeDetails = () => {
  dialog.value = false
  emit('close-details')
}

watch(() => props.movie, (newVal) => {
  dialog.value = !!newVal
})
</script>