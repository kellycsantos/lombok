<template>
  <div class="footer">
    <span class="menu-footer">
      <a v-for="(item, index) in menuFooter" :key="index" :href="item.link">{{
        item.menu
      }}</a>
    </span>
    <span class="icons">
      <a
        v-for="(social, index) in socialNetwork"
        :key="index"
        class="icon"
        :href="social.name"
        ><img :src="require(`../assets/images/icon/${social.icon}.png`)"
      /></a>
    </span>
  </div>
</template>
<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "FooterSection",
  components: {},
  data() {
    return {
      socialNetwork: [
        { name: "Instagram", icon: "instagram" },
        { name: "Twitter", icon: "twitter" },
        { name: "Facebook", icon: "facebook" },
        { name: "Pinterest", icon: "pinterest" },
      ],
      menuFooter: [
        { menu: "Sobre", link: "#about" },
        { menu: "Artigos", link: "#article" },
        { menu: "Inscreva-se", link: "#subscribe" },
      ],
    };
  },
});
</script>
<style>
.footer {
  height: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  padding: 10px 30px;
}

.menu-footer {
  text-align: center;
}
.icons {
  display: flex;
  padding: 10px;
}
.icon {
  width: 30px;
  margin: 5px;
}

@media screen and (min-width: 768px) {
  .footer {
    height: auto;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: 10px 30px;
  }

  .icon img {
    width: 30px;
  }

  .menu-footer {
    display: flex;
    justify-content: space-between;
    width: 40vw;
    text-transform: uppercase;
  }
}
</style>
