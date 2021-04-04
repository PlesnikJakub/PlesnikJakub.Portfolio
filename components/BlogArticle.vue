<template>
  <div class="col-lg-4 col-md-6 col-sm-12 pb-4">
    <div class="card shadow-lg">
      <div class="card-body">
        <!--img class="card-img-top" :src="project.image" alt="Card image cap" /-->
        <div class="card-title">
          <NuxtLink :to="{ name: 'blog-slug', params: { slug: article.slug } }">
            <h5>{{ article.title }}</h5>
          </NuxtLink>
        </div>
        <p>{{ formatDate(article.updatedAt) }}</p>

        <p class="card-text">
          {{ article.description }}
        </p>
      </div>
    </div>
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
      return new Date(date).toLocaleDateString('en')
    },
  },
})
</script>
