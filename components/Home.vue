<template>
  <section id="home" class="sections">
    <div class="home-text">
      <span class="intro-text">Hello, my name is Jakub </span>
      <h1 class="hello-text">
        I'm a
        <transition name="slide-fade">
          <span v-if="visible" class="jobs">{{
            availableWords[currentWord]
          }}</span>
        </transition>
      </h1>
      <p class="paragraph-text">
        <i>
          I'm very passionate and dedicated to my work. With 7 years experience
          as a professional software developer, I have acquired the skills and
          knowledge necessary to make your project a success. I enjoy every step
          of development from designing the system, to actual implementation and
          testing.
        </i>
      </p>
      <div class="col-12 container mt-5">
        <div class="row mt-5">
          <div class="col-8 offset-2 row mt-5">
            <div class="col-1 offset-1">
              <img src="~/assets/github.png" class="img-thumbnail github" />
              <h5 class="name">Github</h5>
            </div>
            <div class="col-1 offset-1">
              <img src="~/assets/twitter.png" class="img-thumbnail github" />
              <h5 class="name">Twitter</h5>
            </div>
            <div class="col-1 offset-1">
              <img src="~/assets/youtube.png" class="img-thumbnail github" />
              <h5 class="name">Youtube</h5>
            </div>
            <div class="col-1 offset-1">
              <img src="~/assets/linkedin.png" class="img-thumbnail github" />
              <h5 class="name">Linkedin</h5>
            </div>
          </div>
        </div>
      </div>
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
        'PhD Student',
      ],
      currentWord: 0,
      visible: true,
    }
  },
  mounted() {
    setInterval(this.onTick, 2000)
  },
  methods: {
    onTick() {
      this.visible = false
      setTimeout(() => (this.visible = true), 1000)
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
.home-text {
  padding-top: 20%;
}
h5.name {
  color: white;
}
.github {
  background: transparent;
  border: none;
}
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
.jobs {
  font-weight: bold;
  color: var(--primary-color);
}
.intro-text {
  color: var(--primary-text-color);
  font-size: 1.5rem;
  font-family: Roboto, sans-serif;
  text-align: left;
  margin-left: 25%;
  margin-right: 10%;
}
.paragraph-text {
  color: var(--disabled-text-color);
  font-size: 1rem;
  font-family: Roboto, sans-serif;
  text-align: left;
  margin-left: 25%;
  margin-right: 10%;
  max-width: 40%;
}
.hello-text {
  color: var(--primary-text-color);
  font-size: 4rem;
  font-family: Roboto, sans-serif;
  text-align: left;
  margin-left: 25%;
  margin-right: 10%;
}
</style>
