<template>
  <v-card class="mx-3 my-5" max-width="344">
    <v-img
      :src= "img"
      height="200px"
    ></v-img>

    <v-card-title> {{ title }} </v-card-title>

    <v-card-subtitle> {{ subtitle }} </v-card-subtitle>

  </v-card>
</template>

<script>
export default {
  name: 'Card2',
  props: ['img', 'title', 'subtitle']
};
</script>