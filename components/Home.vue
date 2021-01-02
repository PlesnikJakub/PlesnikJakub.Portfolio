<template>
  <section id="home" class="sections">
    <div class="home-text" style="padding-top: 20%;">
      <span class="intro-text">Hello, my name is Jakub </span>
      <h1 class="hello-text">
        I'm a
        <transition name="slide-fade">
          <span v-if="visible" class="jobs">{{
            availableWords[currentWord]
          }}</span>
        </transition>
      </h1>
    </div>
  </section>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      availableWords: [
        'Developer',
        'Data Scientist',
        'League of Legends Fan',
        'Phd Student',
      ],
      currentWord: 0,
      visible: true,
    }
  },
  mounted() {
    setInterval(this.onTick, 4000)
  },
  methods: {
    onTick() {
      this.visible = false
      setTimeout(() => (this.visible = true), 1500)
      if (this.currentWord + 1 === this.availableWords.length) {
        this.currentWord = 0
        return
      }
      this.currentWord++
    },
  },
})
</script>

<style scoped>
/* Enter and leave animations can use different */
/* durations and timing functions.              */
.slide-fade-enter-active {
  transition: all 0.5s ease;
}
.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active below version 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}

.intro-text {
  color: white;
  font-size: 1.5rem;
  font-family: Roboto, sans-serif;
  text-align: left;
  margin-left: 25%;
  margin-right: 10%;
}
.hello-text {
  color: white;
  font-size: 4rem;
  font-family: Roboto, sans-serif;
  text-align: left;
  margin-left: 25%;
  margin-right: 10%;
}
</style>
