<template>
 
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <Acomp> </Acomp>
  <Bcomp></Bcomp>
  <Ccomp></Ccomp>

</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Acomp from './components/Acomp.vue'
import Bcomp from './components/Bcomp.vue'
import Ccomp from './components/Ccomp.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    Acomp,
    Bcomp,
    Ccomp
  }
}
</script>

<style>

</style>
