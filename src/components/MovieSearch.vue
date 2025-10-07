<template>
  <v-card class="pa-4" elevation="4" color="#637896">
    <h3 class="text-h5 mb-4 text-center titulo">🔎 Buscar Películas</h3>

    <v-form @submit.prevent="emitSearch">
      <v-text-field
        v-model="query"
        label="Título de la película"
        required
      />

      <v-select
        v-model="type"
        :items="['movie', 'series', 'episode']"
        label="Tipo"
      />

      <v-text-field
        v-model="year"
        label="Año (opcional)"
        type="number"
      />

      <v-btn class="boton" @click="emitSearch">Buscar</v-btn>

      <br></br>
      <br></br>

      <v-btn class="boton" @click="emitClear">Limpiar</v-btn>

    </v-form>
  </v-card>
</template>

<script setup>
import { ref } from 'vue'

const query = ref('')
const type = ref('movie')
const year = ref('')

const emit = defineEmits(['search-movies', 'clear-results'])

const emitSearch = () => {
  if (!query.value.trim()) return
  emit('search-movies', { query: query.value, type: type.value, year: year.value })
}

const emitClear = () => {
  query.value = ''
  type.value = 'movie'
  year.value = ''
  emit('clear-results')
}
</script>

<style scoped>
.titulo{
  font-family: 'Poppins', sans-serif;
  font-weight: 700;
  color: #dad8f4;
  letter-spacing: 2px;
}

.boton {
  color: white !important;
  justify-content: center;
  background-color: #274876 !important;
  border-radius: 50px !important;
  padding: 10px 24px !important;
  transition: all 0.3s ease;
}

.boton:hover {
  background-color: #3d70b7 !important;
}
</style>