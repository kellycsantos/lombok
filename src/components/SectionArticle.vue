<template>
  <div id="article">
    <h2>Ultimos artigos</h2>
    <DividerBar class="divider" />
    <ArticleItems />
  </div>
</template>
<script lang="ts">
import Vue from "vue";
import DividerBar from "./Divider.vue";
import ArticleItems from "./ArticleItems.vue";

export default Vue.extend({
  name: "SectionArticle",
  components: {
    DividerBar,
    ArticleItems,
  },
});
</script>

<style scoped>
#article {
  background: #f2f4f1;
  min-height: 70vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 30px 0;
}

.divider {
  border-width: 2px;
  margin-bottom: 5px;
}
</style>
