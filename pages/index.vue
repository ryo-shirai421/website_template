<template>
  <v-app id="IndexPage">
    <v-main>
      <v-container class="container">
        <CardWithVideo/>
        <Card/>
      </v-container>
    </v-main>
  </v-app>
</template>

<style>
.container {
  width: 95%;
}
</style>


<script>

import CardWithVideo from '~/components/CardWithVideo.vue'
import Card from '~/components/Card.vue'

export default {
  name: 'IndexPage',
  components: {
    CardWithVideo,
    Card,
  }
}
</script>