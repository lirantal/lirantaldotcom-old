<template>
  <v-main>
    <section id="block-quote">
      <v-row justify="center">
        <v-col cols="6">
          <h2 class="v-heading text-h4 text-sm-h4 mb-4">
            Community recognitions and testimonials
          </h2>
          <blockquote>
            <p>
              I'm thankful for being able to take an active part in communities
              I'm passionte about, such as, web security, Node.js engineering
              projects, and building command-line applications. I'm also
              grateful for the opportunity to work with some of the best people
              in the community, including the OWASP community members and
              leadership, the broader Node.js Foundation and the Technical
              Steering Committee members.
            </p>
            <p>
              Perhaps best of all, I'm grateful for the opportunities I have
              through my speaking engagement and other advocacy work that allow
              me to inspire and help others. These are always my greatest source
              of proud moments.
            </p>
          </blockquote>
        </v-col>
      </v-row>
    </section>
    <v-divider></v-divider>
    <v-timeline>
      <v-timeline-item
        v-for="recognition in recognitions"
        :key="recognition.href"
        color="#0084b4"
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
                  class="elevation-6 item-pointer"
                  :alt="recognition.name"
                  :src="recognition.profile_image"
                  @click="openLink('https://twitter.com/manicode')"
                ></v-img>
              </v-list-item-avatar>

              <v-list-item-content>
                <v-list-item-title
                  class="item-pointer"
                  @click="openLink(recognition.contact)"
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
          medium_username: 'manicode',
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
          medium_username: 'jjperezaguinaga',
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
          medium_username: 'cryptus_neoxys',
          profile_image:
            'https://pbs.twimg.com/profile_images/1373856007009411075/Dbfd_Bne_400x400.jpg',
          testimonial: `This has become my primary source for learning docker with node. Thanks for sharing these 💝`,
        },
        {
          type: 'web-security-activism',
          medium: 'twitter',
          href: 'https://twitter.com/fcarrascosa_dev/status/1543694130940870659',
          name: 'Fernando Carrascosa',
          title: 'Tech Lead',
          contact: 'https://twitter.com/fcarrascosa_dev',
          medium_username: 'fcarrascosa_dev',
          profile_image:
            'https://pbs.twimg.com/profile_images/1512047671552450565/fQvrbswJ_400x400.jpg',
          testimonial: `After being in a workshop by @liran_tal and realizing that RegExps can be exploited fairly easily, I decided to use a validation library. I even contributed to the @DefinitelyTyped definition of it :D`,
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
