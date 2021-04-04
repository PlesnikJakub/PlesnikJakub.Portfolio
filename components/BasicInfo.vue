<template>
  <div class="col-6 mb-3">
    <h5>{{ title }}</h5>
    <span>{{ value }}</span>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  props: {
    title: {
      type: String,
      default: '',
    },
    value: {
      type: String,
      default: '',
    },
  },
})
</script>
