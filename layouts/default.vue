<template>
  <v-app dark>
    <BaseNavbar/>
    <v-main style="height:100000px">
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import BaseNavbar from '~/components/BaseNavbar'

export default {
  name: 'DefaultLayout',
  components: {
    BaseNavbar
  },
  data () {
    return {}
  }
}
</script>
