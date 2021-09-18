<template>
  <v-container class="mt-1">
    <v-row>
      <v-col class="text-center">
        <v-avatar size="180">
          <img src="https://github.com/lirantal.png" alt="John" />
        </v-avatar>
      </v-col>
    </v-row>

    <v-row>
      <v-col class="text-center">
        Hello, I'm Liran Tal
        <v-icon medium color="white">mdi-hand-wave-outline</v-icon>
      </v-col>
    </v-row>

    <v-row>
      <v-col class="text-center mb-n5">
        <span class="green--text"> Software Engineer </span>
        ·
        <span class="red--text"> Web Security Activist </span>
        ·
        <span class="yellow--text"> Open Source Software Champion </span>
      </v-col>
    </v-row>

    <v-row>
      <v-col class="text-center">
        <v-btn icon link href="https://twitter.com/liran_tal" target="_blank">
          <v-icon medium> mdi-twitter </v-icon>
        </v-btn>
        <v-btn icon link href="https://github.com/lirantal" target="_blank">
          <v-icon medium> mdi-github </v-icon>
        </v-btn>
        <v-btn
          icon
          link
          href="https://www.linkedin.com/in/talliran/"
          target="_blank"
        >
          <v-icon medium> mdi-linkedin </v-icon>
        </v-btn>
      </v-col>
    </v-row>

    <v-row justify="center">
      <v-col cols="12" lg="10" class="text-center">
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
          >, world-wide recognized for championing open source software and
          actively working within communities to inspire and lift other humans.
          <span
            class="
              mx-1
              item-pointer
              green--text
              font-italic
              text-decoration-underline
            "
            @click="openLink('https://github.com/nodejs/security-wg')"
            >A JavaScript & Node.js software developer, building web
            applications and command-line tools.</span
          >

          <span
            class="
              mx-1
              item-pointer
              red--text
              font-italic
              text-decoration-underline
            "
            @click="openLink('https://owasp.org/www-project-cwe-toolkit')"
            >A web security activist
          </span>
          , engaging in security research, software supply chain security, and
          regular contributor and project lead to OWASP Foundation projects.
          <span
            class="
              mx-1
              item-pointer
              red--text
              font-italic
              text-decoration-underline
            "
            @click="openLink('https://github.com/nodejs/security-wg')"
            >An avid member of the Node.js Foundation ecosystem security working
            group</span
          >, dedicated to advancing Node.js security awareness and skillset in
          the open source community.
          <span
            class="
              mx-1
              item-pointer
              purple--text
              darken-4
              font-italic
              text-decoration-underline
            "
            @click="openLink('https://snyk.io')"
            >Developer Advocate at Snyk</span
          >.
        </blockquote>
      </v-col>
    </v-row>

    <v-row>
      <v-col class="text-center">
        <v-chip class="text-caption ma-1" label> OWASP Project Leader </v-chip>
        <v-chip class="text-caption ma-1" label> Public Spekaer </v-chip>
        <v-chip class="text-caption ma-1" label> O'Reilly Author </v-chip>
        <v-chip class="text-caption ma-1" label>
          Node.js Foundation Security WG Warrior
        </v-chip>
        <v-chip class="text-caption ma-1" label>
          Docker Container Security Hero
        </v-chip>
        <v-chip class="text-caption ma-1" label>
          Command-line Apps Knight
        </v-chip>
      </v-col>
    </v-row>
  </v-container>
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