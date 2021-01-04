<template>
  <div>
    <Scripts />
    <Navigation />
    <div class="container-fluid">
      <div id="Home" class="row sections">
        <div class="col">
          <Home />
        </div>
      </div>
      <div id="About" class="row sections">
        <div class="col">
          <About />
        </div>
      </div>
      <div id="Projects" class="row sections">
        <div class="col">
          <Projects />
        </div>
      </div>
      <div id="Contact" class="row sections">
        <div class="col">
          <Footer />
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Particles from 'particles.vue'

Vue.use(Particles)

export default Vue.extend({})
</script>

<style>
.delimeter {
  border-bottom: 2px solid #ff5900;
  width: 100px;
}
.sections {
  height: 100vh;
  scroll-snap-align: start;
  background: black;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
