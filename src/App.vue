<template>
  
  <NavBar/>
  <HeroPage/>
  <FooTer/>

</template>

<script>
import NavBar from './components/NavBar.vue'
import FooTer from './components/FooTer.vue'
import HeroPage from './components/HeroPage.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    HeroPage,
    FooTer,
    
  }
}
</script>

<style>

</style>
