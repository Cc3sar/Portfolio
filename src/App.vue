<script setup>
  import Navbar from './components/Navbar.vue'
  import FindMe from './components/FindMe.vue'
</script>

<template>
  <div>
    <Navbar />
    <router-view />
    <FindMe />
  </div>
</template>

<style scoped>
  .find-me {
    position: absolute;
    display: flex;
    flex-direction: column;
    top: 85%;
    left: 3%;
  }

</style>