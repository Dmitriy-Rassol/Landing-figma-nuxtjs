<template>
  <v-col>
    <v-container>
      <v-col align="center">
        <video aria-label="Nothing great is made alone" role="heading" aria-level="1"
          src="https://cdn.sanity.io/files/599r6htc/localized/4caa8274fa1a76f5df188b7969c41e2b00890801.mp4" autoplay=""
          playsinline="" style="max-width: 90%;"></video>
        <h3 style="font-weight: 400;">Figma connects everyone in the design process so teams can deliver better products
          faster.</h3>
        <br>
        <v-btn outlined color="black" @click="scrollToForm">
          Sign up free
        </v-btn>
      </v-col>
    </v-container>
    <v-img
      src="https://cdn.sanity.io/images/599r6htc/localized/455e29e0d05e64300b4a2aa99bcd25fa10a341a7-6969x2010.png?rect=0,0,6969,2008&w=2016&h=581&q=75&fit=max&auto=format"
      style="width: 150%;" />
    <v-container>
      <SocialCard />
    </v-container>
    <LastDivider />
    <v-container ref="registerForm">
      <RegisterForm />
    </v-container>
  </v-col>
</template>

<script>
export default {
  name: "IndexPage",
  methods: {
    scrollToForm() {
      const el = this.$refs.registerForm;
      if (el) {
        el.scrollIntoView({ behavior: 'smooth' });
      }
    }
  }
}
</script>
