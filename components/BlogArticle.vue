<template>
  <div class="col-lg-4 col-md-6 col-sm-12 pb-4">
    <NuxtLink :to="{ name: 'blog-slug', params: { slug: article.slug } }">
      <div class="card shadow-lg">
        <div class="card-body">
          <!--img class="card-img-top" :src="project.image" alt="Card image cap" /-->
          <div class="card-title">
            <h5>{{ article.title }}</h5>
          </div>
          <p>{{ formatDate(article.updatedAt) }}</p>

          <p class="card-text">
            {{ article.description }}
          </p>
        </div>
      </div>
    </NuxtLink>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    article: {
      type: Object,
      required: true,
    },
  },
  methods: {
    formatDate(date: string | number | Date) {
      const options = { year: 'numeric', month: 'long', day: 'numeric' }
      return new Date(date).toLocaleDateString('en', options)
    },
  },
})
</script>
