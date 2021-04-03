<template>
  <section id="projects" class="sections">
    <div class="container">
      <div class="row">
        <h2 class="col section-title">Projects</h2>
        <p class="section-subtitle">
          Experience is the mother of wisdom and I think most of the experiences
          for developers comes from different project. These are some projects I
          had oportunity to worked on.
        </p>
      </div>
      <div class="row">
        <Project
          v-for="project in projects"
          :key="project.id"
          :project="project"
        />
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'
const projectsJSON = require('./../assets/projects.json')

export default Vue.extend({
  data() {
    return {
      projectsLoaded: false,
      projects: projectsJSON.projects,
    }
  },
})
</script>
<style scoped>
h2.section-title {
  color: var(--primary-text-color) !important;
}

p.section-subtitle {
  color: var(--secondary-text-color) !important;
}
</style>
