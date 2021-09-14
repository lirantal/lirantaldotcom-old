<template>
  <v-main>
    <v-row>
      <v-col class="text-center">
        <v-avatar size="180">
          <img src="https://github.com/lirantal.png" alt="John" />
        </v-avatar>
      </v-col>
    </v-row>

    <v-row>
      <v-col class="text-center"> Hello, I'm Liran Tal 👋 </v-col>
    </v-row>

    <v-row>
      <v-col class="text-center">
        <v-btn icon link href="https://twitter.com/liran_tal" target="_blank">
          <v-icon medium> mdi-twitter </v-icon>
        </v-btn>
        <v-btn icon link href="https://github.com/lirantal" target="_blank">
          <v-icon medium> mdi-github </v-icon>
        </v-btn>
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
              href="https://github.com/lirantal/dockly"
              target="_blank"
              color="orange"
              text
            >
              Explore
            </v-btn>

            <v-spacer></v-spacer>

            <v-btn icon>
              <v-icon>mdi-heart</v-icon>
            </v-btn>

            <v-btn icon>
              <v-icon>mdi-bookmark</v-icon>
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
              href="https://github.com/lirantal/is-website-vulnerable"
              target="_blank"
              color="orange"
              text
            >
              Explore
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>

      <v-col>
        <v-card class="mx-auto" max-width="360">
          <v-img
            class="white--text align-end"
            src="https://github.com/lirantal/npq/raw/master/.github/npq-demo.gif?raw=true"
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
            <v-btn
              href="https://github.com/lirantal/npq"
              target="_blank"
              color="orange"
              text
            >
              Explore
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-main>
</template>

<script>
export default {
  methods: {
    openLink(url) {
      return window.open(url, '_blank')
    },
  },
}
</script>

<style lang="css" scoped>
.item-pointer {
  cursor: pointer;
}
</style>