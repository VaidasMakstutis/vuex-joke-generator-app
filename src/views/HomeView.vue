<template>
  <div class="shadow-xl bg-gray-200 w-8/12 mx-auto p-20">
    <h2 class="text-3xl text-blue-600 font-extrabold">Can I Haz Dad Jokes</h2>
    <h3 class="h-40 text-black mt-10">{{ joke }}</h3>
    <button @click="addJoke" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full mt-10 focus:outline-none">Add Joke</button>
  </div>
</template>

<script>

import { mapActions, mapGetters } from 'vuex';

export default {
  name: 'HomeView',
  methods: {
    ...mapActions({addJoke: 'setCurrentJoke'}),
  },
  computed: {
    ...mapGetters({joke: 'getCurrentJoke'}),
  },
}
</script>

<style scoped>
h3 {
  height: 100%;
  font-size: 2.5rem;
}
</style> 
