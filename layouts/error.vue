<template>
  <v-app light>
    <v-content>
      <v-container>
        <v-card class="mx-auto yellow darken-2">
          <v-card-title>
            <h1 v-if="error.statusCode === 404">
              {{ pageNotFound }}
            </h1>
            <h1 v-else>
              {{ otherError }}
            </h1>
          </v-card-title>
          <v-card-text>
            <NuxtLink to="/">
              Home page
            </NuxtLink>
          </v-card-text>
        </v-card>
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
export default {
  props: {
    error: {
      type: Object,
      default: null
    }
  },
  data () {
    return {
      pageNotFound: '404 Not Found',
      otherError: 'Sorry! Something went wrong...'
    }
  },
  head () {
    const title =
      this.error.statusCode === 404 ? this.pageNotFound : this.otherError
    return {
      title
    }
  }
}
</script>

<style scoped>
h1 {
  font-size: 20px;
}
</style>
