<template>
  <v-app id="Activity">
    <v-main>
      <v-container class="container text-left">
        <p class="text-left pl-5 mt-5 text-h5 text--primary">年間行事</p>
        <v-card class="mx-auto">
          <v-list>
            <v-list-item-group
              v-model="selected"
              active-class="pink--text"
              multiple
            >
              <pre class="ml-5 pb-3">予定</pre>
              <v-divider></v-divider>
              <template v-for="(item, index) in items">
                <v-list-item :key="item.title">
                </v-list-item>

                <v-divider
                  v-if="index < items.length - 1"
                  :key="index"
                ></v-divider>
              </template>
            </v-list-item-group>
          </v-list>
        </v-card>
      </v-container>
    </v-main>
  </v-app>
</template>

<style>
.container {
  width: 75%;
}
.text-left {
    text-align: left;
}
</style>

<script>
export default {
  data: () => ({
    selected: [2],
    items: [
    ],
  }),
};
</script>
