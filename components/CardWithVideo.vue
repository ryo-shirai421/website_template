<template>
  <v-card class="mx-auto my-5">
    <v-card-text class="text-left">
      <p class="text-h4 text--primary">新入生の皆さんへ</p>
      <div class="text--primary">
        ご入学おめでとうございます。<br />
        「大学で??がしたいんだ!!」という新入生の入部をお待ちしております。
      </div>
    </v-card-text>
    <div class="youtube">
      <iframe
        width="100%"
        height="400"
        src="https://www.youtube.com/embed/UfbGPz-6DBQ?autohide=1&showinfo=0&color=white&rel=0&vq=highres&modestbranding=1&fs=0"
        frameborder="0"
        allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>
    </div>
    <v-card-actions>
      <v-btn
        text
        color="teal accent-4"
        @click="reveal = true"
        to="section/activity"
      >
        新入生の皆さんへ
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  name: "CardWithVideo",
};
</script>
