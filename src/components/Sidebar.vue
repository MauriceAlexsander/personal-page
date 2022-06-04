<template>
  <Transition name="sidebar-animation">
    <div @click.prevent="closeSidebar()" v-if="props.isExtended" class="sidebar-container">
      <div class="sidebar">
        <div class="header">
          <p @click="closeSidebar()">+</p>
          <ExternalLinks />
        </div>

        <div class="routes">
          <router-link @click.prevent="closeSidebar()" to="/">Home</router-link>
          <router-link @click.prevent="closeSidebar()" to="/about">About</router-link>
          <router-link @click.prevent="closeSidebar()" to="/stack">My Stack</router-link>
          <router-link @click.prevent="closeSidebar()" to="/contact">Contact</router-link>
        </div>
      </div>
    </div>
  </Transition>
</template>

<script lang="ts" setup>
import { defineProps, defineEmits } from 'vue';
import ExternalLinks from "./ExternalLinks.vue";
const emit = defineEmits(['closeSidebar'])

// Props
const props = defineProps({isExtended: Boolean})

const closeSidebar = () => emit('closeSidebar')

</script>

<style scoped>
.sidebar-animation-enter-active {
  animation: disappear 0.5s reverse;
}

.sidebar-animation-leave-active {
  animation: disappear 0.5s;
}

.sidebar-animation-enter-active .sidebar {
  animation: disappear-sidebar 0.5s;
}

.sidebar-animation-leave-active .sidebar {
  animation: disappear-sidebar 0.5s reverse;
}

@keyframes disappear {
  from {
    visibility:visible;
    opacity: 1;
  }
  to {
    visibility: hidden;
    opacity: 0;
  }
}

@keyframes disappear-sidebar {
  from {
    margin-left: -120px;
    visibility: hidden;
    opacity: 0;
  }
  to {
    margin-left: 0px;
    visibility:visible;
    opacity: 1;
  }
}


.sidebar-container {
  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background: none;
  backdrop-filter: none;
  background: rgba(0, 0, 0, 0.2);
  backdrop-filter: blur(8px);
}

.sidebar {
  position: fixed;
  display: flex;
  flex-direction: column;
  top: 0;
  left: 0;
  height: 100%;
  width: 320px;
  background: var(--darker-green);
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-direction: row;
  height: 72px;
  width: 100%;
  background: var(--dark-green);
  padding: 0 12px;
}

.header p {
  color: gray;
  font-size: 32px;
  font-weight: 500;
  transform: rotate(45deg);
  transition: 0.2s;
  margin: 0;
}

.header p:hover {
  color: white;
  cursor: pointer;
}

.routes {
  padding: 24px;
  display: flex;
  flex-direction: column;
  text-align: start;
}

.routes a {
  text-decoration: none;
  color: white;
  font-size: 18px;
  padding: 12px 0;
}

.routes a.router-link-exact-active {
  color: var(--light-green);
}

.extented {
  animation-name: appear;
  animation-fill-mode: forwards;
} 

.extented .sidebar {
  animation-name: appear-sidebar;
  animation-fill-mode: forwards;
}

</style>
