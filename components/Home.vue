<template>
    <v-container>
    <v-row >
      <v-col v-for="personaje in personajes"
          :key="personaje.id" cols="12" md="6" lg="4">
        <v-card class="mx-auto" max-width="344">
          <v-img
            :src="personaje.imagen"
            height="200px"
          ></v-img>

          <v-card-title> {{personaje.nombre}}</v-card-title>
        </v-card>
      </v-col>
      
    </v-row>
  </v-container>
</template>
<script>
export default {
  name: "Home",

  data: () => ({
    personajes: [
      {
        id: 1,
        nombre: "Morty",
        imagen: "https://rickandmortyapi.com/api/character/avatar/2.jpeg",
      },
      {
        id: 2,
        nombre: "Rick",
        imagen: "https://rickandmortyapi.com/api/character/avatar/1.jpeg",
      },
      {
        id: 3,
        nombre: "Summer",
        imagen: "https://rickandmortyapi.com/api/character/avatar/3.jpeg",
      },
      {
        id: 4,
        nombre: "Beth",
        imagen: "https://rickandmortyapi.com/api/character/avatar/4.jpeg",
      },
      {
        id: 5,
        nombre: "Jerry",
        imagen: "https://rickandmortyapi.com/api/character/avatar/5.jpeg",
      },
    ],
  }),
};
</script>