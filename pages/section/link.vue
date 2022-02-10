<template>
  <v-app id="Link">
    <v-main>
      <v-container class="d-flex align-start flex-wrap">

        <SimpleCard :img="img" :title="title" :subtitle="subtitle"/>

        <SimpleCard :img="img2" :title="title" :subtitle="subtitle"/>
        <SimpleCard :img="img2" :title="title" :subtitle="subtitle"/>
        <SimpleCard :img="img2" :title="title" :subtitle="subtitle"/>
        <SimpleCard :img="img2" :title="title" :subtitle="subtitle"/>
        <SimpleCard :img="img2" :title="title" :subtitle="subtitle"/>
        <SimpleCard :img="img2" :title="title" :subtitle="subtitle"/>

      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import SimpleCard from "~/components/SimpleCard.vue";

export default {
  components: {
    SimpleCard,
  },
  
  data() {
    return {
      img: "https://cdn.vuetifyjs.com/images/cards/sunshine.jpg",
      img2: "https://cdn.pixabay.com/photo/2020/07/12/07/47/bee-5396362_1280.jpg",
      title: "hello world",
      subtitle: "1,000 miles of wonder"
    };
  },
};
</script>
