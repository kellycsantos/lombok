<template>
  <div id="about">
    <img src="../assets/images/Plants Glass.jpg" alt="" />
    <div class="about-us">
      <h2>Sobre nós</h2>
      <Divider class="divider" />
      <p>
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ad
        exercitationem temporibus nihil, explicabo doloremque nulla natus eum
        facere doloribus vel esse, perspiciatis ducimus odio tempora repudiandae
        autem eaque. Soluta accusamus autem, blanditiis quae molestiae
        asperiores!
      </p>
    </div>
  </div>
</template>
<script lang="ts">
import Vue from "vue";
import Divider from "./Divider.vue";

export default Vue.extend({
  name: "AboutUs",
  components: {
    Divider,
  },
});
</script>
<style>
#about {
  display: flex;
  flex-direction: column;
  text-align: center;
}

.about-us {
  min-height: 300px;
}
.about-us p {
  padding: 10px 15px;
}
.about img {
  width: 100%;
  height: 300px;
}

@media screen and (min-width: 768px) {
  #about img {
    width: 50vw;
    height: 100%;
  }
  #about {
    display: flex;
    flex-direction: row;
    height: 40vh;
  }

  .about-us {
    width: 50vw;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .about-us p {
    padding: 10px 65px;
  }
}
</style>
