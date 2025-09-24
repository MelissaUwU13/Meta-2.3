<template>
<br></br>
  <v-table class="tabla">
    <thead>
      <tr>
        <th class="text-left">
          Caracteristicas
        </th>
        <th class="text-left">
          Uso en Japón
        </th>
        <th class="text-left">
          Curiosidades
        </th>
      </tr>
    </thead>
    <tbody>
      <tr
        v-for="item in datos"
        :key="item.dato1"
      >
        <td>{{ item.dato1 }}</td>
        <td>{{ item.dato2 }}</td>
        <td>{{ item.dato3 }}</td>
      </tr>
    </tbody>
  </v-table>
  <br></br>
</template>

<script setup>
  const datos = [
    {
      dato1: 'Árbol ornamental de flores rosadas',
      dato2: 'Celebraciones de Hanami',
      dato3: 'Sus flores duran solo 1-2 semanas'
    },
    {
      dato1: 'Existen más de 200 variedades',
      dato2: 'Decoración de calles y templos',
      dato3: 'Algunas especies tienen flores blancas'
    }
  ]
</script>

<style scoped>
.tabla{
margin: 20px auto;           /* centra la tabla */
  max-width: 800px;            /* limita ancho */
  border-collapse: collapse;   /* bordes unidos */
  border: 2px solid #D93F9F;   /* borde exterior */
  background-color: #F5B0DC; 
}

th, td{
width: 250px;
padding: 5px;
border: 2px solid #D93F9F;
}
</style>