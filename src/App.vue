<template>
<div id="app">
  <nav id="nav" class="flex justify-between max-w-xl mx-auto text-2xl">
    <router-link to="/">Home</router-link> |
    <router-link to="/jokes">All Jokes</router-link>
  </nav>
  <router-view/>
</div>
</template>

<script>

import { mapActions } from 'vuex';

export default {
  methods: {
    ...mapActions(['setCurrentJoke'])
  },
  mounted() {
    this.setCurrentJoke();
  }
}
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 60px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
