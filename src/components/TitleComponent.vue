<template>
  <div class="title">
    <h1>Lombok</h1>
    <h2>Holistic Health</h2>
    <DividerBar class="divider" />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import DividerBar from "./Divider.vue";

export default Vue.extend({
  name: "TitleComponent",
  components: {
    DividerBar,
  },
});
</script>

<style scoped>
.title {
  height: 50vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.divider {
  display: inline-block;
  border: 3.5px solid #436b43;
  border-radius: 8px;
  width: 75px;
  margin-top: 5px;
}

@media screen and (min-width: 768px) {
  .title h1 {
    font-size: 82px;
  }
  .title h2 {
    font-size: 30px;
  }
}
</style>
