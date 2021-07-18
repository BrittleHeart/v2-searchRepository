<template>
  <section class="results p-4 bg-gray-700">
    <ul v-if="results.items">
      <li v-for="result in results.items" :key="result.id"> {{ result.owner.login }}</li>
    </ul>
  </section>
</template>

<script>
import { ref } from 'vue'

export default {
  props: [
    'results'
  ],
}
</script>

<style>
.results {
  width: 100%;
  height: 600px;
  max-height: 700px;
  overflow-y: scroll;
}
</style>