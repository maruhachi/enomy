<template>
  <section class="container">
    <div>
      <h1 class="title">Pictures</h1>
      <h2 class="subtitle">you can (not) gather picture from &#34;eshi&#34;</h2>
    </div>
    <div>
      <p>{{ host }}</p>
      <p>{{ content }}</p>
      <button @click="fetchData">UUIDリクエスト</button>
    </div>
    <div class="tile is-vertical">
      <div class="tile">
        <tweet/>
      </div>
    </div>
  </section>
</template>

<script>
import tweet from "~/components/Tweet.vue";

export default {
  components: {
    tweet
  },
  created: function() {
    this.fetchData();
  },
  watch: {
    $route: "fetchData"
  },
  data() {
    return {
      host: "",
      content: ""
    };
  },
  methods: {
    async fetchData() {
      const response = await this.$axios.$get("https://httpbin.org/uuid");
      this.content = response.uuid;
    }
  },
  async asyncData({ app }) {
    const response = await app.$axios.$get("https://httpbin.org/get");
    return { host: response.headers.Host };
  }
};
</script>

<style scoped>
</style>
