<template>
  <v-app light>
    <profile-Header />
    <nuxt />
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
