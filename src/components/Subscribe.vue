<template>
  <div id="subscribe">
    <h2>Inscreva-se</h2>
    <InputEmail />
  </div>
</template>
<script lang="ts">
import Vue from "vue";
import InputEmail from "./SubscribeForm.vue";

export default Vue.extend({
  name: "SubscribeSection",
  components: {
    InputEmail,
  },
  data() {
    return {};
  },
  methods: {},
});
</script>

<style>
#subscribe {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 55vh;
  text-align: center;
  background: #dfe4de;
  padding: 0 15px;
}

#subscribe h2 {
  font-size: 35px;
}
</style>
