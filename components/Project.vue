<template>
  <div class="col-lg-4 col-md-6 col-sm-12 pb-4">
    <div class="card shadow-lg">
      <div class="card-body">
        <h5 class="card-title">{{ project.title }}</h5>
        <p class="card-text">
          {{ project.description }}
        </p>
        <p class="card-text">
          <small class="text-muted">
            <span
              v-for="technology in project.technologies"
              :key="technology"
              class="btn-sm btn-dark"
              >{{ technology }}</span
            >
          </small>
        </p>
        <a
          v-for="link in project.links"
          :key="link"
          :href="link.link"
          target="_blank"
          class="btn btn-primary card-link"
          >{{ link.name }}</a
        >
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    project: {
      type: Object,
      required: true,
    },
  },
})
</script>
