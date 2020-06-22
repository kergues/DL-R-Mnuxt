<template>
  <v-layout>
      <v-row>
      <v-col cols="12" sm="12" md="8" offset-md="2">
        <v-card color="lime lighten-1">
          <v-container fluid>
            <v-row>
              <v-col
                v-for="personaje in personajes"
                :key="personaje.id"
                class="d-flex child-flex"
                cols="12"
                md="4"
                sm="6"
                xs="12"
              >
                <v-hover>
                  <template v-slot="{ hover }">
                    <v-card flat class="d-flex" :elevation="hover ? 24 : 6">
                      <v-img
                        :src="personaje.imagen"
                        aspect-ratio="1"
                        class="black--text"
                      >
                        <v-row
                          class="fill-height"
                          align="center"
                          justify="center"
                          align-content="end"
                        >
                          <v-card-title>{{ personaje.nombre }}</v-card-title>
                        </v-row>
                      </v-img>
                    </v-card>
                  </template>
                </v-hover>
              </v-col>
            </v-row>
          </v-container>
        </v-card>
      </v-col>
    </v-row>
  </v-layout>
</template>

<script>
export default {
  data: () => ({
    personajes: [
      {
        id: 1,
        nombre: "Morty",
        imagen: "https://rickandmortyapi.com/api/character/avatar/2.jpeg"
      },
      {
        id: 2,
        nombre: "Rick",
        imagen: "https://rickandmortyapi.com/api/character/avatar/1.jpeg"
      },
      {
        id: 3,
        nombre: "Summer",
        imagen: "https://rickandmortyapi.com/api/character/avatar/3.jpeg"
      },
      {
        id: 4,
        nombre: "Beth",
        imagen: "https://rickandmortyapi.com/api/character/avatar/4.jpeg"
      },
      {
        id: 5,
        nombre: "Jerry",
        imagen: "https://rickandmortyapi.com/api/character/avatar/5.jpeg"
      },
      {
        id: 6,
        nombre: "Abadango",
        imagen: "https://rickandmortyapi.com/api/character/avatar/6.jpeg"
      }
    ]
  })
};
</script>

<style lang="scss" scoped></style>