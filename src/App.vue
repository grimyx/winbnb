<template>
  <div class="main-container">
    <SearchStays class=".search"/>
  </div>
</template>

<script setup>

import SearchStays from './components/SearchStays.vue';


</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

.main-container {
  padding: 2rem;
}
</style>
