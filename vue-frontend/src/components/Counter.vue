<template>
  <div>
    <button v-on:click="count += 1">Increment</button>
    <button v-on:click="count -= 1">Decrement</button>
    <p>Episodes seen: {{ count }}.</p>
  </div>
</template>

<script>
export default {
  props: { count: Number }
};
</script>

<style>
</style>

