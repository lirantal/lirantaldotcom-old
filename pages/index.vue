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
      <v-col cols="7" class="text-center">
        <blockquote class="blockquote">
          A
          <span
            class="
              mx-1
              item-pointer
              yellow--text
              font-italic
              text-decoration-underline
            "
            @click="openLink('https://stars.github.com/profiles/lirantal')"
            >GitHub Star</span
          >
          recognized for activisim in open source communities and advancing web
          and Node.js security. Member of the Node.js Foundation ecosystem
          security working group, Project lead and contributor to the OWASP
          Foundation, and Developer Advocate at Snyk.
        </blockquote>
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