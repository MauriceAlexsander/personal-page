<template>
  <div class="nav-container sticky-top">
    <div class="container">
      <div id="nav">
        <a class="menu-button" @click="isExtended = true">
          <div></div>
          <div></div>
          <div></div>
        </a>

        <router-link class="home-btn" to="/">Home</router-link>

        <div class="pages">
          <router-link to="/about">About</router-link>
          <router-link to="/stack">My Stack</router-link>
          <router-link to="/contact">Contact</router-link>
        </div>

        <ExternalLinks/>
      </div>

      <Sidebar v-if="mobile" @closeSidebar="isExtended = false" :isExtended="isExtended"/>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { Ref, ref } from 'vue';
import ExternalLinks from './ExternalLinks.vue';
import Sidebar from '@/components/Sidebar.vue';
import { useBreakpoints } from '@vueuse/core';

const breakpoints = useBreakpoints({desktop: 1081,})
const mobile = breakpoints.smaller('desktop')

// Data
const isExtended: Ref<boolean> = ref(false)
</script>

<style scoped>
.nav-container{
  background: var(--black);
}
#nav {
  display: flex;
  justify-content: space-between;
  position: -webkit-sticky;
  align-items: center;
  height: 72px;
  width: 100%;
}

#nav a {
  font-weight: bold;
  color: white;
  text-decoration: none;
  transition: 0.3s;
}

.menu-button {
  display: none;
  justify-content: space-between;
  padding-left: 12px;
  flex-direction: column;
  height: 18px;
  width: 96px;
  cursor: pointer;
}

.menu-button div {
  height: 2px;
  width: 24px;
  background: white;
}

.home-btn {
  font-weight: bold;
  font-size: 24px;
  width: 96px;
}

#nav a.router-link-exact-active {
  color: var(--light-green);
}

.pages {
  display: flex;
  justify-content: space-around;
  width: 540px;
}

@media screen and (max-width: 1080px){
  .menu-button {
    display: flex;
  }

  .home-btn {
    display: none;
  }

  .pages {
    display: none;
  }
}
</style>
