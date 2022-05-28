<template>
  <div id="initial">
    <NavBar />
    <TitleComponent />
  </div>
</template>
<script lang="ts">
import Vue from "vue";
import NavBar from "./NavBar.vue";
import TitleComponent from "./TitleComponent.vue";

export default Vue.extend({
  name: "InitialSection",
  components: {
    NavBar,
    TitleComponent,
  },
});
</script>

<style scoped>
#initial {
  margin: 15px;
  background: url("../assets/images/background.jpg") #e8e7e3 left bottom
    no-repeat;
  background-size: cover;
  height: 70vh;
}

@media screen and (min-width: 768px) {
  #initial {
    background: url("../assets/images/background.jpg") #e8e7e3 left bottom
      no-repeat;
    background-size: contain;
  }
}
</style>
