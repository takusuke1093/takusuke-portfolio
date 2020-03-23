<template>
  <v-app light>
    <profile-Header />
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <profile-footer />
  </v-app>
</template>

<script>
export default {
  components: {
    profileFooter: () => import('~/components/footer'),
    profileHeader: () => import('~/components/header')
  },
  data () {
    return {
    }
  }
}
</script>
