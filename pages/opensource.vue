<template>
  <v-main>
    <v-row>
      <v-col>
        <v-card class="greeting-card" min-height="100%">
          <v-row class="ma-0 pa-0">
            <v-col>
              <v-card-title class="pt-1 ps-2">
                Liran Tal is a GitHub Star
                <v-icon class="ml-1" color="yellow"> mdi-star </v-icon>
              </v-card-title>
              <v-card-subtitle class="ps-2">
                <p>
                  On June, 2021, Liran was officially recognized and awarded to
                  GitHub's world-wide influencers Stars program.
                </p>

                <p>
                  Liran is the first, and currently the only member of the
                  GitHub Stars program to be recognized in Israel 🇮🇱
                </p>
              </v-card-subtitle>
            </v-col>

            <v-col cols="3">
              <v-img
                contain
                height="120"
                src="https://uxwing.com/wp-content/themes/uxwing/download/24-sport-and-awards/trophy.png"
                class="greeting-card-bg"
              ></v-img>
            </v-col>
          </v-row>
          <v-row class="ma-0 pa-0">
            <v-col>
              <v-card-actions class="d-flex align-center pb-2 ps-2">
                <div>
                  <p class="text-xl font-weight-semibold primary--text mb-2">
                    Inspire. Educate. Shape communities.
                  </p>

                  <v-btn
                    href="https://twitter.com/github/status/1405191446232289287"
                    target="_blank"
                    small
                    color="primary"
                  >
                    View on Twitter
                  </v-btn>
                </div>
              </v-card-actions>
            </v-col>
          </v-row>
        </v-card>
      </v-col>

      <v-col>
        <v-card min-height="100%">
          <v-card-title class="align-start">
            <span>GitHub open source contribution activity</span>
            <v-spacer></v-spacer>
          </v-card-title>

          <v-card-subtitle class="mb-2">
            <v-btn icon small class="mr-2">
              <v-icon> mdi-github </v-icon>
            </v-btn>
            <span class="font-weight-semibold text--primary"
              >https://github.com/lirantal</span
            >
          </v-card-subtitle>

          <v-card-text>
            <v-row>
              <v-col>
                <v-avatar size="80">
                  <img src="https://github.com/lirantal.png" alt="Liran Tal" />
                </v-avatar>
              </v-col>
              <v-col
                v-for="data in statisticsData"
                :key="data.title"
                class="d-flex align-center"
              >
                <v-avatar color="black" rounded class="elevation-1">
                  <v-icon dark :color="data.color">
                    {{ data.icon }}
                  </v-icon>
                </v-avatar>
                <div class="ms-3">
                  <p class="text-xs mb-0">
                    {{ data.title }}
                  </p>
                  <h3 class="text-xl font-weight-semibold">
                    {{ data.total }}
                  </h3>
                </div>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>

      <v-col>
        <v-card min-height="100%">
          <v-card-title class="align-start">
            <span>Relevany programming languages & technology stack</span>
          </v-card-title>

          <v-card-subtitle class="mb-6"> </v-card-subtitle>

          <v-card-text>
            <v-row>
              <v-col>
                <div>
                  <p>Node.js</p>
                  <v-progress-linear
                    v-model="langNodeJSXP"
                    color="green darken-3"
                  ></v-progress-linear>
                  <p>JavaScript</p>
                  <v-progress-linear
                    v-model="langJavaScriptXP"
                    color="yellow accent-4"
                  ></v-progress-linear>
                  <br />
                </div>
                <div>
                  <v-icon medium> mdi-nodejs </v-icon>
                  <v-icon medium> mdi-npm </v-icon>
                  <v-icon medium> mdi-language-javascript </v-icon>
                  <v-icon medium> mdi-language-html5 </v-icon>
                  <v-icon medium> mdi-vuejs </v-icon>
                  <v-icon medium> mdi-vuetify </v-icon>
                  <v-icon medium> mdi-vs-code </v-icon>
                  <v-icon medium> mdi-bash </v-icon>
                  <v-icon medium> mdi-docker </v-icon>
                  <v-icon medium> mdi-firebase </v-icon>
                </div>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>

    <v-row>
      <v-col class="text-center">
        <v-divider></v-divider>
      </v-col>
    </v-row>

    <v-row>
      <v-col class="text-center">
        <p>
          Following are some of my most well known open source projects that you
          can find on GitHub:
        </p>
      </v-col>
    </v-row>

    <v-row justify="center">
      <v-col>
        <v-card class="mx-auto" max-width="360">
          <v-img
            class="white--text align-end"
            src="https://repository-images.githubusercontent.com/71667498/d5576f00-69cd-11e9-83dd-2139ad967fdc"
          >
          </v-img>

          <v-card-title>dockly</v-card-title>

          <v-card-text class="text--primary">
            <div>
              Immersive terminal interface for managing docker containers and
              services
            </div>
          </v-card-text>

          <v-card-actions>
            <v-btn
              icon
              href="https://github.com/lirantal/dockly"
              target="_blank"
            >
              <v-icon>mdi-github</v-icon>
            </v-btn>

            <v-btn icon>
              <v-icon>mdi-share-variant</v-icon>
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>

      <v-col>
        <v-card class="mx-auto" max-width="360">
          <v-img
            class="white--text align-end"
            src="https://github.com/lirantal/is-website-vulnerable/raw/master/.github/is-website-vulnerable-logo.png"
          >
          </v-img>

          <v-card-title>is-website-vulnerable</v-card-title>

          <v-card-text class="text--primary">
            <div>
              finds publicly known security vulnerabilities in a website's
              frontend JavaScript libraries
            </div>
          </v-card-text>

          <v-card-actions>
            <v-btn
              icon
              href="https://github.com/lirantal/is-website-vulnerable"
              target="_blank"
            >
              <v-icon>mdi-github</v-icon>
            </v-btn>

            <v-btn icon>
              <v-icon>mdi-share-variant</v-icon>
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>

      <v-col>
        <v-card class="mx-auto" max-width="360">
          <v-img
            class="white--text align-end"
            src="https://repository-images.githubusercontent.com/114298694/73d29f00-bb7d-11e9-80f5-5f94f25a76b4"
          >
          </v-img>

          <v-card-title>npq</v-card-title>

          <v-card-text class="text--primary">
            <div>
              🎖safely* install packages with npm or yarn by auditing them as
              part of your install process
            </div>
          </v-card-text>

          <v-card-actions>
            <v-btn icon href="https://github.com/lirantal/npq" target="_blank">
              <v-icon>mdi-github</v-icon>
            </v-btn>

            <v-btn icon>
              <v-icon>mdi-share-variant</v-icon>
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-main>
</template>

<script>
export default {
  data() {
    const statisticsData = [
      {
        title: 'Total Repositories',
        total: '298',
        icon: 'mdi-github',
        color: 'white',
      },
      {
        title: 'Total Stars',
        total: '10.9k',
        icon: 'mdi-star-shooting-outline',
        color: 'yellow',
      },
      {
        title: 'Total PRs',
        total: '1.1k',
        icon: 'mdi-source-pull',
        color: 'green',
      },
      {
        title: 'Contributed to',
        total: '47 repos',
        icon: 'mdi-code-tags',
        color: 'blue',
      },
    ]

    return {
      statisticsData,
      langJavaScriptXP: 100,
      langNodeJSXP: 100,
    }
  },

  methods: {
    openLink(url) {
      return window.open(url, '_blank')
    },
  },
}
</script>

<style lang="scss" scoped>
.item-pointer {
  cursor: pointer;
}
</style>