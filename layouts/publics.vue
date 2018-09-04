
<template>
  <v-app>
    <v-navigation-drawer v-model="drawer" app right>
      <v-list>
          <v-list-tile v-for="item in items" :key="item.title">
            <v-list-tile-action>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title><nuxt-link :to="item.url">{{ item.title }}</nuxt-link></v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </v-list>
        </v-navigation-drawer>
<<<<<<< HEAD
    
    <v-content>
      <nuxt/>
    </v-content>
    <v-footer class="grey darken-4">
    <v-spacer></v-spacer>
    <div>&copy; {{ new Date().getFullYear() }}</div>
  </v-footer>
=======
    <v-toolbar app class="grey darken-4">
      <v-toolbar-title></v-toolbar-title>
      <v-spacer/>
      <v-toolbar-side-icon @click.stop="drawer = !drawer"/>

    </v-toolbar>
    <v-content>
      <nuxt/>
    </v-content>
>>>>>>> 5337246e06bb02ae9678accc05efd792ca88febb
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      items: [
         { title: 'Home', icon: 'home', url: '/' },
         { title: 'Room', icon: 'android', url: '/table' },
         { title: 'Profile', icon: 'group', url: '/profile' },
<<<<<<< HEAD
         { title: 'search', icon: 'security', url: '/search' },
=======
         { title: 'key', icon: 'security', url: '/keyroom' },
>>>>>>> 5337246e06bb02ae9678accc05efd792ca88febb
      
       ],
     }
  },
  computed: {
    online: {
      get() {
        return this.$store.state.online
      },
      set(value) {
        this.$store.commit('setOnline', value)
      },
    },
    drawer: {
      get() {
        return this.$store.state.drawer
      },
      set(value) {
        this.$store.commit('setDrawer', value)
      },
    },
  },

  mounted() {
    this.$store.commit('setOnline', window.navigator.onLine)
    window.addEventListener('offline', this.toggleNetworkStatus)
    window.addEventListener('online', this.toggleNetworkStatus)
  },

  beforeDestroyed() {
    window.removeEventListener('offline', this.toggleNetworkStatus)
    window.removeEventListener('online', this.toggleNetworkStatus)
  },

  methods: {
    toggleNetworkStatus({ type }) {
      this.online = type === 'online'
    },
  },
}
</script>
