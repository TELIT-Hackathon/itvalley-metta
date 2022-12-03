<template>
  <div class="about">
    <h1>This is an about page</h1>
    <p>{{count}}</p>
    <button @click="increment">123</button>
    <p>{{doubleCount}}</p>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>

<script>
import { computed } from '@vue/reactivity'

  export default {
  data() {
    return {
      count: 1
    }
  },

  // `mounted` is a lifecycle hook which we will explain later
  mounted() {
    // `this` refers to the component instance.
    console.log(this.count) // => 1

    // data can be mutated as well
    this.count = 2
  },
  methods : {
    increment(){
      this.count++
    }
  },
  
  computed : {
    doubleCount(){
      return this.count*2
    }
  }
}
</script>
