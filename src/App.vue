<template>
  <Navbar />
  
  <router-view style="height: 100%;"/>
</template>

<script lang="ts" setup>
import Navbar from '@/components/Navbar.vue'
</script>

<style>
:root {
  --black: #272727;
  --darker-green: #223829;
  --dark-green: #1C482C;
  --green: #17592E;
  --light-green: #00DC82;
}

body {
  margin: 0;
  background: var(--black);
}

#app {
  font-family: 'Courier New', Courier, monospace;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background: var(--black);
  color: white;
}

.opacity {
  opacity: 0;
}

.appear-animation {
  animation-name: block-appear;
  animation-duration: 1s;
  animation-fill-mode: forwards;
}

@keyframes block-appear {
  from {
    opacity: 0;
    transform: translateY(100px);
  }
  to {
    opacity: 1;
  }
}

</style>
