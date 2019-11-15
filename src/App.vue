<template>
  <div>
   <app-navbar></app-navbar>
   <app-home></app-home>
  </div>
</template>

<script>
import NavBar from './components/core/NavBar';
import Home from './components/Home';

export default {
  components:{
    'app-navbar':NavBar,
    'app-home':Home
  }
}
</script>

<style scoped>

</style>

