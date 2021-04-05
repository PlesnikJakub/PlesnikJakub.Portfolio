<template>
  <footer id="Blog" class="site-footer">
    <div class="container">
      <hr />
      <div class="row">
        <h1>Blog Posts</h1>
        <ul>
          <li v-for="article of articles" :key="article.slug">
            <BlogArticle :article="article" />
          </li>
        </ul>
      </div>
      <hr />
    </div>
  </footer>
</template>
<script>
export default {
  async fetch() {
    this.articles = await this.$content('articles')
      .only(['title', 'description', 'img', 'slug', 'author'])
      .sortBy('createdAt', 'asc')
      .fetch()
  },
  data() {
    return {
      articles: [],
    }
  },
}
</script>
<style scoped>
.site-footer {
  scroll-snap-align: end;
}
</style>
