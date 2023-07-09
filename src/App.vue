<script setup>
import MapComponent from './components/MapComponent.vue';
import SearchBox from './components/SearchBox.vue';
import ResultCard from './components/ResultCard.vue'
</script>

<template>
  <div class="container mx-auto">
    <div class="relative z-10">
      <img class="hidden sm:block w-full" src="./assets/images/pattern-bg-desktop.png" alt="">
      <img class="block sm:hidden" src="./assets/images/pattern-bg-mobile.png" alt="">
      <div class="absolute w-full top-0">
        <SearchBox />
      </div>
      <ResultCard />
    </div>
    <MapComponent />
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
