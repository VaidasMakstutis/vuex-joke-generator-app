<template>
<div>
  <h1 class="text-3xl p-12 font-extrabold">This is list of all jokes!</h1>
  <h4 v-for="(joke, index) in jokes" :key=index>
    <span>{{ index+1 }}.</span>
    {{ joke }}
  </h4>
</div>
</template>

<script>
import { mapGetters } from 'vuex';

export default {
    computed: {
        ...mapGetters({
            jokes: 'getAllJokes'
        })
    }
}
</script>

<style scoped>
h4 {
    color: blueviolet;
    font-weight: bolder;
    font-size: 2.5rem;
}
</style>