<template>
  <div class="article-items">
    <span v-for="(article, index) in articles" :key="index" class="cards">
      <img :src="require(`../assets/images/${article.image}.jpg`)" />
      <DividerBar class="divider" />
      <p>{{ article.resume }}</p>
    </span>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import DividerBar from "./Divider.vue";

export default Vue.extend({
  name: "ArticleItems",
  components: {
    DividerBar,
  },
  data() {
    return {
      title: "teste",
      articles: [
        {
          image: "Green aesthetic",
          resume: "Dolor sit amet consectetur adipisicing elinumquam a alias",
        },
        {
          image: "Nature Aesthetic Girl",
          resume: "Fugit accusantium, pariceat esse impedit eum!",
        },
        {
          image: "Nature Aesthetic",
          resume: "Voluptatum mestiae, alias voluptates ",
        },
      ],
    };
  },
});
</script>

<style scoped>
.article-items {
  display: flex;
  flex-direction: column;
}
img {
  width: 250px;
  height: 70%;
  transition: 0.3s;
  cursor: pointer;
}

img:hover {
  filter: grayscale(95%);
}

.cards {
  margin: 10px;
  height: 345px;
  text-align: center;
  box-shadow: 2px 2px 10px rgb(145, 145, 145);
  border-radius: 3px;
  background: #fbfbfb;
  width: 250px;
}

.cards p {
  padding: 0 5px;
}

.divider {
  border-width: 1.2px;
  width: 25px;
  margin-bottom: 5px;
}

@media screen and (min-width: 768px) {
  .article-items {
    display: flex;
    flex-direction: row;
  }
}
</style>
