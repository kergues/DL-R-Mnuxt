<template>
  <v-footer color="grey darken-3" padless>
    <v-row justify="center" no-gutters>
      <v-btn
        v-for="item in items"
        :key="item"
        color="white"
        text
        rounded
        class="my-2"
      >
        {{ item }}
      </v-btn>
      <v-col class="grey darken-4 py-4 text-center white--text" cols="12">
        {{ new Date().getFullYear() }} — <strong>Rick & Morty</strong>
      </v-col>
    </v-row>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    items: ["Welcome", "Origen", "Lista"]
  })
};
</script>
