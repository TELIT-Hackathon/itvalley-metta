<script>
import { RouterLink, RouterView } from 'vue-router'

export default {
  data() {
    return {
      count: 1
    }
  },


  methods : {
    singinpopup(){
      this.count++
    }
  }
}
  

</script>

<template>
      <nav>
        <RouterLink to="/"><img src="../assets/icon.svg" alt=""></RouterLink>
        
        <button class="sing"  @click="singinpopup">Sign in</button>
        <p>{{count}}</p>
      </nav>
</template>


<style lang="scss" scoped>

</style>