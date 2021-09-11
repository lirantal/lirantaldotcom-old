<template>
  <v-app dark fixed>
    <v-bottom-navigation>
      <v-btn>
        <span>GitHub Star</span>
        <v-icon color="yellow">mdi-star</v-icon>
      </v-btn>

      <v-btn>
        <span>Developer Advocate</span>
        <v-icon color="green">mdi-heart</v-icon>
      </v-btn>

      <v-btn>
        <span>Projects</span>
        <v-icon>mdi-code-tags</v-icon>
      </v-btn>

      <v-btn>
        <span>Security Activist</span>
        <v-icon color="purple">mdi-security</v-icon>
      </v-btn>
    </v-bottom-navigation>

    <v-main>
      <v-container mt-16>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      title: 'Liran Tal',
    }
  },
}
</script>
