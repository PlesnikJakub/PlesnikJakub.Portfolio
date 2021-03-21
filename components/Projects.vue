<template>
  <section id="projects" class="sections">
    <div class="container">
      <div class="row">
        <h2 class="col text-white">Projects</h2>
        <p class="lead text-white">
          I believe projects are the best way to learn. These are some projects
          I had oportunity to worked on.
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
