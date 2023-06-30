<script setup>
  import Navbar from './components/Navbar.vue'
  import FindMe from './components/FindMe.vue'
</script>

<template>
    <Navbar />
    <main>
      <router-view />
    </main>
    <FindMe />
</template>