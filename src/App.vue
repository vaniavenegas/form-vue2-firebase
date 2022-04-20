<template>
  
  <div class="container">
    <NavBar/>
    <router-view/>
  </div>
  
</template>

<script>
import { mapActions } from 'vuex'
import NavBar from './components/NavBar.vue'
  export default {
    components: {
      NavBar
    },
    methods:{
      ...mapActions(['cargarLocalStorage'])
    },
    created(){
      this.cargarLocalStorage()
    }
    
  }

</script>

<style>

</style>
