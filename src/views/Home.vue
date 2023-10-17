<template>
  <v-container style="min-height: inherit">
    <v-row class="text-center" style="min-height: inherit">
      <v-col cols="12">
        <v-img
            :src="require('../assets/ALiggesmeyer.png')"
            class="my-3"
            contain
            height="100"
        />
      </v-col>

      <v-col
          class="mb-5"
          cols="12"
      >
        <person-card v-for="(person, i) in persons"
                     :value="person"
                     :key="i"
        ></person-card>
      </v-col>

      <v-col
          class="mb-5"
          cols="12"
      >
        <h2 class="headline font-weight-bold mb-3">
          Services
        </h2>

        <v-row justify="center">
          <v-btn
              class="ma-2"
              v-for="(link, i) in importantLinks"
              :key="i"
              x-large
              outlined
              target="_blank"
              :href="link.href"
              style="text-transform: none; background-color: rgba(255,255,255,0.22)"
          >
            <v-icon x-large>
              {{ link.icon }}
            </v-icon>
            {{ link.text }}
          </v-btn>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>

import PersonCard from "@/components/PersonCard";
import {mdiGithub, mdiWeb, mdiLinkedin, mdiWeatherCloudy, mdiGoogleController, mdiCogRefreshOutline} from "@mdi/js";

export default {
  name: 'Home',
  components: {PersonCard},
  data: () => {
    return {
      persons: [
        {
          name: 'Alexander Liggesmeyer',
          subtitle: 'Student',
          links: [
            {
              icon: mdiWeb,
              href: 'https://alexander.liggesmeyer.net'
            }, {
              icon: mdiGithub,
              href: 'https://github.com/alex9849'
            }, {
              icon: mdiLinkedin,
              href: 'https://www.linkedin.com/in/alexander-liggesmeyer/'
            }
          ]
        }
      ],
      importantLinks: [
        {
          icon: mdiWeatherCloudy,
          href: 'https://cloud.liggesmeyer.net',
          text: 'Cloud'
        }
      ]
    }
  }
}
</script>
