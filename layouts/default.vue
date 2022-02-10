<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >

      <h2 class="text-center py-5">大阪大学??部</h2>
      <v-divider></v-divider>

      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      
      <v-btn
        icon
        @click.stop="clipped = !clipped"
      >
        <v-icon>mdi-application</v-icon>
      </v-btn>
      
      <v-toolbar-title v-text="title" />
      <v-spacer />
      
    </v-app-bar>
    
    <Nuxt />  
    
    <v-navigation-drawer
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light>
              mdi-repeat
            </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'ホーム',
          to: '/'
        },
        {
          icon: 'mdi-city',
          title: '部活紹介',
          to: '/section/activity'
        },
        {
          icon: 'mdi-account-multiple',
          title: 'メンバー',
          to: '/section/member'
        },
        {
          icon: 'mdi-clock-time-four-outline',
          title: 'スケジュール',
          to: '/section/schedule'
        },
        {
          icon: 'mdi-calendar-range',
          title: '試合結果',
          to: '/section/result'
        },
        {
          icon: 'mdi-school',
          title: 'OB・OG',
          to: '/section/graduate'
        },
        {
          icon: 'mdi-link',
          title: 'リンク',
          to: '/section/link'
        },
        {
          icon: 'mdi-information-outline',
          title: 'お問い合わせ',
          to: '/section/form'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: '大阪大学??部'
    }
  }
}
</script>
