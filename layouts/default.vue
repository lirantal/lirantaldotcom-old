<template>
  <v-app dark fixed>
    <v-container>
      <v-card dark color="#121212" class="d-flex mb-6" flat tile>
        <v-card dark color="#121212" elevation="0" class="mr-auto pa-2" tile>
          <v-btn>
            <v-icon>mdi-home</v-icon>
            <span>Home</span>
          </v-btn>
        </v-card>

        <v-card dark color="#121212" elevation="0" class="pa-2" tile>
          <v-btn
            href="https://stars.github.com/profiles/lirantal"
            target="_blank"
          >
            <v-icon class="text-body-1" color="yellow">mdi-star</v-icon>
            <span class="text-caption">GitHub Star</span>
          </v-btn>
        </v-card>

        <v-card dark color="#121212" elevation="0" class="pa-2" tile>
          <v-btn>
            <v-icon class="text-body-1" color="green">mdi-heart</v-icon>
            <span class="text-caption">Developer Advocate</span>
          </v-btn>
        </v-card>

        <v-card dark color="#121212" elevation="0" class="pa-2" tile>
          <v-btn>
            <v-icon class="text-body-1" color="blue">mdi-code-tags</v-icon>
            <span class="text-caption">Open Source</span>
          </v-btn>
        </v-card>
      </v-card>
    </v-container>

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
