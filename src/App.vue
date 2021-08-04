<template>
 
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <Acomp> </Acomp>
  <Bcomp></Bcomp>

</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Acomp from './components/Acomp.vue'
import Bcomp from './components/Bcomp.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    Acomp,
    Bcomp
  }
}
</script>

<style>

</style>
