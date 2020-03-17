<template>
  <v-footer
    dark
    padless
  >
    <v-card
      flat
      tile
      class="indigo lighten-1 white--text text-center"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
        メールでの連絡がつきやすいです．経歴の詳細などはlinkedInをご参照ください．
        また，お仕事のご依頼は現在受け付けておりません．予めご了承ください．
        メールでの連絡がつきやすいです．経歴の詳細などはlinkedInをご参照ください．
        また，お仕事のご依頼は現在受け付けておりません．予めご了承ください．
        メールでの連絡がつきやすいです．経歴の詳細などはlinkedInをご参照ください．
      </v-card-text>

      <v-divider />

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
import '@fortawesome/fontawesome-free/css/all.css'
export default {
  data: () => ({
    icons: [
      'fab fa-github',
      'fab fa-google',
      'fab fa-linkedin',
      'fab fa-instagram'
    ]
  })
}
</script>

<style>

</style>
