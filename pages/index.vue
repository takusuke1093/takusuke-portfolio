
<template>
  <div id="app">
    <v-content>
      <section id="hero">
        <v-row no-gutters>
          <v-img
            :min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
            :src="require('@/assets/images/home.jpg')"
          >
            <v-theme-provider dark>
              <v-container fill-height>
                <v-row
                  align="center"
                  class="white--text mx-auto"
                  justify="center"
                >
                  <v-col
                    class="white--text text-center pl-0"
                    cols="12"
                    tag="h2"
                  >
                    <span
                      :class="[$vuetify.breakpoint.mdAndDown ? 'display-2': 'display-4']"
                      class="font-weight-black text-center"
                    >
                      @takusuke1093
                    </span>
                  </v-col>

                  <v-btn
                    class="align-self-end"
                    fab
                    outlined
                    @click="$vuetify.goTo('#about-me')"
                  >
                    <v-icon>mdi-chevron-double-down</v-icon>
                  </v-btn>
                </v-row>
              </v-container>
            </v-theme-provider>
          </v-img>
        </v-row>
      </section>

      <section id="about-me">
        <div class="py-12" />

        <v-container class="text-center">
          <h2 class="display-2 font-weight-bold mb-3">
            ABOUT ME
          </h2>

          <v-responsive
            class="mx-auto mb-8"
            width="56"
          >
            <v-divider class="mb-1" />

            <v-divider />
          </v-responsive>

          <v-responsive
            class="mx-auto title font-weight-light mb-8"
            max-width="720"
          >
            @takusuke1093<br>
            Front-end Web Developer<br>
            Student at Tokyo University of Science
          </v-responsive>

          <v-avatar
            class="elevation-12 mb-12"
            size="128"
          >
            <v-img :src="require('@/assets/images/profile.jpg')" />
          </v-avatar>

          <div />

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
        </v-container>

        <div class="py-12" />
      </section>

      <section
        id="features"
        class="grey lighten-3"
      >
        <div class="py-12" />

        <v-container class="text-center">
          <h2 class="display-2 font-weight-bold mb-3 font--black">
            SKILLS
          </h2>

          <v-responsive
            class="mx-auto mb-12"
            width="56"
          >
            <v-divider class="mb-1" />

            <v-divider />
          </v-responsive>

          <v-row>
            <v-col
              v-for="({ icon, title, text }, i) in features"
              :key="i"
              cols="12"
              md="4"
              color="indigo lighten-1"
            >
              <v-card
                light
                class="py-12 px-4"
                flat
              >
                <v-theme-provider>
                  <div>
                    <v-avatar
                      color="yellow darken-2"
                      size="88"
                    >
                      <v-icon
                        large
                        color="white"
                        v-text="icon"
                      />
                    </v-avatar>
                  </div>
                </v-theme-provider>

                <v-card-title
                  class="justify-center font--black text-uppercase"
                  v-text="title"
                />

                <v-card-text
                  class="subtitle-1 font--black"
                  color="black"
                  v-text="text"
                />
              </v-card>
            </v-col>
          </v-row>
        </v-container>

        <div class="py-12" />
      </section>

      <section id="stats">
        <v-parallax
          :height="$vuetify.breakpoint.smAndDown ? 700 : 500"
          :src="require('@/assets/images/_DSC4594.jpg')"
        >
          <v-container fill-height>
            <v-row class="mx-auto">
              <v-col
                v-for="[value, title] of stats"
                :key="title"
                cols="12"
                md="3"
              >
                <div class="text-center">
                  <div
                    class="display-3 font-weight-black mb-4"
                    v-text="value"
                  />

                  <div
                    class="title font-weight-regular text-uppercase"
                    v-text="title"
                  />
                </div>
              </v-col>
            </v-row>
          </v-container>
        </v-parallax>
      </section>

      <section id="blog">
        <div class="py-12" />

        <v-container>
          <h2 class="display-2 font-weight-bold mb-3 text-uppercase text-center">
            Blog
          </h2>

          <v-responsive
            class="mx-auto mb-12"
            width="56"
          >
            <v-divider class="mb-1" />

            <v-divider />
          </v-responsive>

          <v-row>
            <v-col
              v-for="({ src, text, title }, i) in articles"
              :key="i"
              cols="12"
              md="4"
            >
              <v-img
                :src="require(`@/assets/images/${src}`)"
                class="mb-4"
                height="275"
                max-width="100%"
              />

              <h3
                class="font-weight-black mb-4 text-uppercase"
                v-text="title"
              />

              <div
                class="title font-weight-light mb-5"
                v-text="text"
              />

              <v-btn
                class="ml-n4 font-weight-black"
                text
                href="/inProgress"
              >
                Continue Reading
              </v-btn>
            </v-col>
          </v-row>
        </v-container>

        <div class="py-12" />
      </section>
    </v-content>
  </div>
</template>

<script>
export default {
  data () {
    return {
      articles: [
        {
          src: 'summer.jpg',
          title: 'My first Internship!',
          text: 'Guess What? I got offered a summer internship  as a React.js front-end engineer! It surprised me a lot because I could not implement...'
        },
        {
          src: 'summary.jpg',
          title: 'Summary of my career',
          text: 'I was seriously thinking my future career should be related to Japanese-Chinese-English translator until graduation from junior high...'
        },
        {
          src: 'book.jpg',
          title: 'until aiming to become Engineer',
          text: 'I would try if I could talk to my past self about what I do now. He won’t believe even half of what I tell him. My surrounding has extremely changed for the past two years…'
        }
      ],
      features: [
        {
          icon: 'mdi-vuejs',
          title: 'Vue.js',
          text: 'Engaged in creating Vue.js Admin Dashboards project as an internship for 3months+. Introduced vuex, vue-router and Vuesax collaborating Rails API with Axios. Created responsive profile page with Nuxt.js and Vuetify.js as a private project.'
        },
        {
          icon: 'mdi-language-ruby-on-rails',
          title: 'Ruby on Rails',
          text: 'Created API for Admin Dashboards project as an internship for 1m+. Implemented some functions like Rspec, fixtures, session, preventing CSRF attacks. Introduced some features with rails gems like Ransack, Kaminari. Creatd simple CRUD app as a private project.'
        },
        {
          icon: 'mdi-account-voice',
          title: 'Consulting skills',
          text: '2y+ experiences as a consultant at an electrical appliance store. Belonged to information solutions division. Troubleshot 100+ bugs and concerns on PC and Broadband-internet-related. Ranked top number of sales of PC’s In the metropolitan area in FY2018/3.'
        }
      ],
      stats: [
        ['JP', 'Nationality'],
        ['2y', 'Overseas life'],
        ['3', 'languages'],
        ['10+', 'Blogs']
      ],
      icons: [
        ['fab fa-github', 'https://github.com/takusuke1093'],
        ['fab fa-google', 'https://mail.google.com/mail/?view=cm&to=takumi.yoshida.seattle@gmail.com'],
        ['fab fa-linkedin', 'https://www.linkedin.com/in/takumi-yoshida/'],
        ['far fa-paper-plane', 'https://github.com/takusuke1093']
      ]
    }
  }
}
</script>

<style lang="scss">
  .font--black{
    color: #121212;
  }
</style>
