<template>
  <v-app>
    
    <v-app-bar clipped-left fixed app>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
    </v-app-bar>
    
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    
    <v-navigation-drawer v-model="drawer" right app temporary fixed />
    
    <v-footer :fixed="fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
    
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Nuxt-boilerplate',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      title: 'Nuxt-boilerplate'
    }
  }
}
</script>
