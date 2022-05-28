<template>
  <div>
    <InitialSection />
    <SectionArticle />
    <AboutUs />
    <SubscribeSection />
    <FooterSection />
  </div>
</template>

<script lang="ts">
import Vue from "vue";

import InitialSection from "./components/SectionInitial.vue";
import SectionArticle from "./components/SectionArticle.vue";
import AboutUs from "./components/AboutUs.vue";
import SubscribeSection from "./components/Subscribe.vue";
import FooterSection from "./components/Footer.vue";

export default Vue.extend({
  name: "App",

  components: {
    InitialSection,
    SectionArticle,
    AboutUs,
    SubscribeSection,
    FooterSection,
  },

  data: () => ({
    //
  }),
});
</script>
<style>
* {
  margin: 0;
  padding: 0;
  list-style: none;
  text-decoration: none;
  color: #161716;
  font-family: "Vazirmatn", sans-serif;
}

h2 {
  font-weight: 200;
  text-transform: uppercase;
}
</style>
