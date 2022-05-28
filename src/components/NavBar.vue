<template>
  <div id="menu">
    <h1>LO</h1>
    <img
      @click="btnOpen"
      class="menu-icon"
      src="../assets/images/icon/menu.png"
    />
    <ul :class="menuOpen ? '' : 'menu-close'">
      <li><a class="link-menu" href="#about">Sobre</a></li>
      <li><a class="link-menu" href="#article">Artigos</a></li>
      <li><a class="link-menu subs-link" href="#subscribe">Inscreva-se</a></li>
    </ul>
  </div>
</template>
<script lang="ts">
import Vue from "vue";

export default Vue.extend({
  name: "NavBar",
  data() {
    return {
      menuOpen: false,
    };
  },
  methods: {
    btnOpen() {
      this.menuOpen = !this.menuOpen;
    },
  },
});
</script>
<style>
#menu {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 80px;
}

.menu-icon {
  display: flex;
  position: absolute;
  right: 7vw;
  z-index: 2;
}

ul,
li,
a {
  display: flex;
  flex-direction: column;
}

.link-menu {
  position: relative;
  top: 70px;
  right: 0px;
  height: 30px;
  width: 250px;
  z-index: 1;
  text-align: center;
  line-height: 30px;
  margin: 5px 0;
  text-transform: uppercase;
  border: 1px solid black;
}

.menu-close {
  display: none;
}

@media screen and (min-width: 768px) {
  #menu {
    justify-content: space-between;
    align-items: center;
  }

  .menu-icon {
    display: none;
  }

  .menu-close {
    display: flex;
  }

  ul,
  li,
  a {
    display: flex;
    flex-direction: row;
  }

  .link-menu {
    margin: 0 5px;
    height: 30px;
    width: 130px;
    align-items: center;
    justify-content: center;
    position: initial;
    border: none;
  }

  .subs-link {
    border: 1px solid black;
  }
}
</style>
