<template>
  <v-app dark>
    <nuxt />
    <profile-footer />
  </v-app>
</template>

<script>
export default {
  components: {
    profileFooter: () => import('~/components/footer')
  },
  data () {
    return {
    }
  }
}
</script>
