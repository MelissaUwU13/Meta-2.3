<template> 
<v-row justify="center"> 
    <v-col cols="12" md="4" class="tarjeta"> 
        <v-card>
        <v-img
          src="/cerezos1.jpg"
          height="200"
          cover
        />
        <v-card-title>Cultura japonesa</v-card-title>
        <v-card-text>
          Ver los cerezos en flor, también conocido como 'hanami', es una tradición profundamente arraigada en Japón donde la gente se reúne para disfrutar de la belleza de las flores y celebrar la llegada de la primavera.
        </v-card-text>
        </v-card> 
    </v-col> 
        
    <v-col cols="12" md="4" class="tarjeta"> 
        <v-card>
        <v-img
          src="/cerezos2.png"
          height="200"
          cover
        />
        <v-card-title>Tipos de flores de cerezo</v-card-title>
        <v-card-text>
          Aunque cada flor de cerezo recibe el nombre de 'sakura', existen variedades con diferentes características, como el color y la forma de la flor.
        </v-card-text>
      </v-card>
    </v-col> 
</v-row> 
</template>

<style scoped>
.tarjeta {
  border: 1px solid #ccc;
  padding: 10px;
  margin: 10px;
  text-align: center;
}
</style>