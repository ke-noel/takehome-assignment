<template>
  <!-- PART 4: Add your code here -->
  <div>
    <p>{{ name }}</p>
    <p>{{ id }}</p>
    <Counter v-bind:count="episodes_seen"/>
    <br>
  </div>
</template>

<script>
import Counter from "./Counter.vue";

// PART 4: Add your code here
export default {
  components: {
    Counter
  },
  props: {
    key: Number,
    id: Number,
    name: String,
    episodes_seen: Number
  }
};
</script>

<style>
</style>
