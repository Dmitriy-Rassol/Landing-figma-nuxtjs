<template>
  <v-app dark>

    <div v-if="announce" class="announce">
      <v-container>
        <v-row class="d-flex align-center justify-center">
          <span>What makes collaboration click? A new research report by Figma.</span>
          <v-btn icon @click="closeAnnounce">
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-row>
      </v-container>
    </div>
    <v-main>
      <v-row class="d-flex justify-space-between" style="padding:0 30px; margin-top:30px;">
        <a href="/">
          <FigmaLogo />
        </a>
        <div>
          <a href="/pricing">
            Pricing
          </a>
        </div>
      </v-row>
      <Nuxt />
    </v-main>
    <v-footer app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
import FigmaLogo from '~/components/FigmaLogo.vue';
export default {
  name: "DefaultLayout",
  components: { FigmaLogo },
  data() {
    return {
      announce: true,
      items: [
        {
          icon: "mdi-apps",
          title: "Welcome",
          to: "/"
        },
        {
          icon: "mdi-chart-bubble",
          title: "Inspire",
          to: "/inspire"
        }
      ],
      title: "Vuetify.js"
    };
  },
  methods: {
    closeAnnounce() {
      this.announce = false;
    }
  }
}
</script>

<style>
.announce {
  background-color: rgb(252, 221, 236);
}
</style>
