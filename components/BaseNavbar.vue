<template>
  <div>
    <v-app-bar
      app
      class="light-blue white--text"
      dense
    >
      <v-app-bar-nav-icon/>

      <v-toolbar-title
        class="text-uppercase"
      >
        {{ $route.name === 'index' ? 'home page' : $route.name }}
      </v-toolbar-title>

      <nuxt-link :to="'/profile'" tag="v-toolbar-title">
        <v-toolbar-title class="mx-3 ">
          <v-btn class="text-capitalize light-blue" dark>
            Profile
          </v-btn>
        </v-toolbar-title>
      </nuxt-link>
      <nuxt-link
        v-for="(link ,i) in computedLinks"
        :key="i"
        :to="`/${link.name}`"
        tag="v-toolbar-title"
      >
        <v-toolbar-title>
          <v-btn class="text-capitalize light-blue" dark depressed fab small>
            <v-icon>
              {{ link.icon }}
            </v-icon>
          </v-btn>
        </v-toolbar-title>
      </nuxt-link>
    </v-app-bar>
  </div>
</template>
<script>
export default {
  name: 'BaseNavbar',
  data () {
    return {
      drawer: false
    }
  },
  computed: {
    computedLeftLinks () {
      return [
        {
          name: 'home',
          icon: 'mdi-home',
          tooltip: 'Home page',
          textColorClass: 'white--text',
          bgColorClass: 'light-blue',
          inUse: true,
          isPopup: false,
          isDropdown: {}
        },
        {
          name: 'profile',
          icon: 'mdi-account-box',
          tooltip: 'Your profile',
          textColorClass: 'white--text',
          bgColorClass: 'light-blue',
          inUse: true,
          isPopup: false,
          isDropdown: {}
        },
        {
          name: 'projects',
          icon: 'mdi-folder-multiple',
          tooltip: 'Your projects',
          textColorClass: 'white--text',
          bgColorClass: 'light-blue',
          inUse: true,
          isPopup: false,
          isDropdown: {}
        },
        {
          name: 'workplace',
          icon: 'mdi-notebook-plus',
          tooltip: 'Bot constructor workplace',
          textColorClass: 'white--text',
          bgColorClass: 'light-blue',
          inUse: true,
          isPopup: false,
          isDropdown: {}
        },
        {
          name: 'alerts',
          icon: 'mdi-bell',
          tooltip: 'Your alerts',
          textColorClass: 'white--text',
          bgColorClass: 'light-blue',
          inUse: true,
          isPopup: false,
          isDropdown: {}
        },
        {
          name: 'settings',
          icon: 'mdi-bell',
          tooltip: 'Your alerts',
          textColorClass: 'white--text',
          bgColorClass: 'light-blue',
          inUse: true,
          isPopup: true,
          isDropdown: {}
        }
      ]
    },
    computedRightLinks () {
      return [
        {
          name: 'logIn',
          icon: 'mdi-login',
          tooltip: 'Log in',
          textColorClass: 'white--text',
          bgColorClass: 'light-blue',
          inUse: true,
          isPopup: true,
          isDropdown: {}
        },
        {
          name: 'logOut',
          icon: 'mdi-logout',
          tooltip: 'Log out',
          textColorClass: 'white--text',
          bgColorClass: 'light-blue',
          inUse: true,
          isPopup: true,
          isDropdown: {}
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>
