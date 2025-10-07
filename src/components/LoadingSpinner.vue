<template>
  <div v-if="loading" class="text-center my-8">
    <v-progress-circular
      indeterminate
      color="primary"
      size="64"
    />
    <p class="mt-2">Cargando...</p>
  </div>
</template>

<script setup>
const props = defineProps({
  loading: {
    type: Boolean,
    required: true
  }
})
</script>
