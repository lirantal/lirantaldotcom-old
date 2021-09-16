<template>
  <v-main>
    <v-timeline>
      <v-timeline-item
        color="#0084b4"
        v-for="recognition in recognitions"
        :key="recognition.href"
      >
        <v-card class="mx-auto" color="" dark max-width="600">
          <v-card-title> </v-card-title>

          <v-card-text class="font-weight-medium">
            <!-- <v-icon medium color="#e9f5fd"> mdi-format-quote-open </v-icon> -->
            {{ recognition.testimonial }}
            <!-- <v-icon medium color="#e9f5fd"> mdi-format-quote-close </v-icon> -->
          </v-card-text>

          <v-card-actions>
            <v-list-item class="grow">
              <v-list-item-avatar color="grey darken-3">
                <v-img
                  @click="openLink('https://twitter.com/manicode')"
                  class="elevation-6 item-pointer"
                  :alt="recognition.name"
                  :src="recognition.profile_image"
                ></v-img>
              </v-list-item-avatar>

              <v-list-item-content>
                <v-list-item-title
                  @click="openLink(recognition.contact)"
                  class="item-pointer"
                  >{{ recognition.name
                  }}<span v-if="recognition.title"
                    >, {{ recognition.title }}</span
                  ></v-list-item-title
                >
              </v-list-item-content>

              <v-row align="center" justify="end">
                <v-btn :href="recognition.href" target="_blank" icon>
                  <v-icon medium color="#08a0e9">
                    mdi-{{ recognition.medium }}
                  </v-icon>
                </v-btn>
                <span class="subheading"></span>
              </v-row>
            </v-list-item>
          </v-card-actions>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </v-main>
</template>

<script>
export default {
  data() {
    return {
      recognitions: [
        {
          type: 'web-security-activism',
          medium: 'twitter',
          href: 'https://twitter.com/manicode/status/1326929685553451008?s=20',
          name: 'Jim Manico',
          title: 'OWASP Leader',
          contact: 'https://twitter.com/manicode',
          profile_image:
            'https://pbs.twimg.com/profile_images/1128010737580818432/cw4SWqUx_400x400.jpg',
          testimonial: `What an honor. Thank you Liran. Some people talk about AppSec (me)
            and some people really dig in and do the work (you). I’m a big fan.
            🤙🏻`,
        },
        {
          type: 'web-security-activism',
          medium: 'twitter',
          href: 'https://twitter.com/jjperezaguinaga/status/1349368415014825989',
          name: 'Jose Aguinaga',
          title: 'Head of Engineering at @hoprnet',
          contact: 'https://twitter.com/jjperezaguinaga',
          profile_image:
            'https://pbs.twimg.com/profile_images/620137226232397824/-bCZ07sG_400x400.jpg',
          testimonial: `This is one of the best guides I've seen on this topic, really cool stuff. Definitely going to take a look at @snyksec's @github action to add it in our @hoprnet project.`,
        },
        {
          type: 'web-security-activism',
          medium: 'twitter',
          href: 'https://twitter.com/cryptus_neoxys/status/1393221416175034369',
          name: 'Dev Sharma',
          title: 'Software Developer',
          contact: 'https://twitter.com/cryptus_neoxys',
          profile_image:
            'https://pbs.twimg.com/profile_images/1373856007009411075/Dbfd_Bne_400x400.jpg',
          testimonial: `This has become my primary source for learning docker with node. Thanks for sharing these 💝`,
        },
      ],
    }
  },
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