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
<style scoped>
.technologies span {
  margin: 3px;
}
.card {
  background: var(--primary-paper-color);
  color: var(--primary-text-color);
  height: 100%;
}
.card-text {
  text-align: justify;
  color: var(--secondary-text-color);
}
.card-img-top {
  max-height: 200px;
  object-fit: fill;
}
.card .card-title {
  color: var(--primary-contrast-color);
}

.btn-dark {
  background: var(--secondary-color-dark) !important;
}

h5 {
  margin-bottom: 0;
  margin-top: 1.25rem;
}
</style>
