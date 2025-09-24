<template>
  <v-container class="text-center">
    <v-row justify="center">

      <v-col cols="12" md="4" sm="6">
        <v-btn class="boton" rounded="xl" size="x-large" href="https://www.viverosshangai.es/10-cosas-que-no-sabias-acerca-del-arbol-de-cerezo" target="_blank" block>Da click para mas informacion</v-btn>
      </v-col>
    </v-row>
  </v-container>

  <br></br>

  <v-footer class="text-center d-flex flex-column ga-2 py-4" color=#F569BF>

    <v-divider class="my-2" thickness="2" width="50"></v-divider>

    <div class="text-caption font-weight-regular opacity-60">
      Esta es una practica utilizando vuetify realizando lo ya hecho en la meta 2.1
    </div>

    <v-divider></v-divider>

    <div>
      {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
    </div>
  </v-footer>

</template>

<style scoped>
.boton{
justify-content: center;
padding:10px;
color: white;
background-color:#F569BF;
outline: none;
text-decoration:none;
border-color: #F569BF;
border-radius: 80px;
}

.boton:hover {
  background-color: #d94a9c; /* un poco más oscuro al pasar el mouse */
}

</style>