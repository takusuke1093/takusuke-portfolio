<template>
  <v-footer
    dark
    padless
  >
    <v-card
      flat
      tile
      class="indigo lighten-1 white--text text-center"
      width="100%"
    >
      <v-card-text>
        <v-btn
          v-for="[icon, src] of icons"
          :key="icon"
          class="mx-4 white--text"
          :href="src"
          icon
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
        Contact me via LinkedIn or Email. takumi.yoshida.seattle@gmail.com
      </v-card-text>

      <v-divider />

      <v-card-text class="white--text">
        Copyright (c) 2020 takusuke1093
        Released under the MIT license. For more details, see <a href="https://github.com/takusuke1093/takusuke-portfolio/blob/master/MITLicense.txt" class="white--text"><u>MITLicense.txt</u></a>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
import '@fortawesome/fontawesome-free/css/all.css'
export default {
  data: () => ({
    icons: [
      ['fab fa-github', 'https://github.com/takusuke1093'],
      ['fab fa-google', 'https://mail.google.com/mail/?view=cm&to=takumi.yoshida.seattle@gmail.com'],
      ['fab fa-linkedin', 'https://www.linkedin.com/in/takumi-yoshida/'],
      ['far fa-paper-plane', 'https://mail.google.com/mail/?view=cm&to=takumi.yoshida.seattle@gmail.com']
    ]
  })
}
</script>

<style>
a{
  color: white;
}

</style>
