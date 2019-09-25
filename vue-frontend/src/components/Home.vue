<template>
  <div>
    <!-- PART 1: Pass in a "complete" prop here -->
    <Instructions v-bind:complete="true"></Instructions>
    <!-- PART 4: Modify the Show component to accept all of these props -->
    <Show
      v-for="show in shows"
      :key="show.id"
      :id="show.id"
      :name="show.name"
      :episodes_seen="show.episodes_seen"
    />
    <p>Add a new show:</p>
    <form @submit.prevent="submit">
      <input type="text" v-model="name" placeholder="name">
       <button v-on:click="newShow(name)">Submit</button>
    </form>
  </div>
</template>

<script>
import Instructions from "./Instructions.vue";
import Show from "./Show.vue";

export default {
  components: {
    Instructions,
    Show
  },
  data() {
    return {
      shows: [
        { id: 1, name: "Game of Thrones", episodes_seen: 0 },
        { id: 2, name: "Naruto", episodes_seen: 220 },
        { id: 3, name: "Black Mirror", episodes_seen: 3 }
      ]
    };
  },
  methods: {
    newShow: function (name) {
      this.shows.push({ id: this.shows[this.shows.length-1].id + 1, name: name, episodes_seen: 0 })
    }
  }
};
</script>

<style>
</style>


