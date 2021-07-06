<template>
  <Default :title="doc.title">
    <nuxt-content :document="doc" />
  </Default>
</template>


<script>
import Counter from "~/components/Counter";

export default {
  head() {
    return {
      titleTemplate: `%s`,
      title: "Nuxt Content Example",
    };
  },
  components: { Counter },
  async asyncData({ $content, params }) {
    const doc = await $content("index").fetch();
    return { doc };
  },
};
</script>