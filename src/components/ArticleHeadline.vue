<template>
  <g-link :to="`/article/${article.id}`" class="headline-item py-3 flex items-center">
    <g-image class="w-20 mx-5" :alt="article.title" :src="article.heroImage.file.url" />
    <div class="text-md">{{article.title}}</div>
    <div v-if="isPopular" class="tag ml-auto">Popular</div>
  </g-link>
</template>

<script>
import { Vue, Component, Prop } from "vue-property-decorator";
import { Article } from "@/models/article";
import { Constant } from "@/utility/constant";

export default {
  props: {
    article: Object,
    isPopular: Boolean
  }
}
</script>

<style scoped>

</style>
