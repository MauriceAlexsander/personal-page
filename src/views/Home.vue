<template>
  <div class="home d-flex flex-column justify-content-center align-items-center">
    <div class="initial-container container d-flex flex-row justify-content-between align-items-center">
      <div class="appear-animation d-flex flex-column align-items-start">
        <h4>Hi, I am</h4>
        <h1 style="text-align: start;">Maurice A. Zanotelli</h1>
        <h3 style="text-align: start; color: var(--light-green)">Keep Moving Forward</h3>
      </div>
      
      <Octahedron class="appear-animation"/>
    </div>

    <div class="who-am-i content">
      <div style="animation-delay: 1s;" class="opacity container appear-animation">
        <h1>Who Am I?</h1>
        <h4>I am a young web developer. Currently I am focused on frontend, but I have knowledge and experience with backend too. It's been 2 years since I started programming web pages, and from the beging I already used Vue as my go-to JavaScript Framework. Today I mainly use Vue 3 + TypeScript with Pinia e Vue Router, and in the backend side, python with Django and FastAPI</h4>
      </div>
    </div>

    <div class="background content">
      <div style="animation-delay: 2s;" class="opacity container appear-animation">
        <h1>Background</h1>
        <h4>Finished school 2018</h4>
        <h4>Joined College 2019</h4>
        <h4>First programmer job 2020 to present (Front-end Engineer)</h4>
      </div>
    </div>

    <div class="code-snippets content">
      <div style="animation-delay: 3s;" class="opacity container appear-animation">
        <h2>My Other Projects</h2>

        <div class="codes d-flex flex-column">
          <a href="https://github.com/MauriceAlexsander/element-follow-cursor" target="_blank">element-follow-cursor</a>
          <a href="https://github.com/MauriceAlexsander/3d-cylinder-visualizer-canvas" target="_blank">3d-cylinder-visualizer-canvas</a>
          <a href="https://github.com/MauriceAlexsander/real-time-chat" target="_blank">real-time-chat (Incomplete)</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import Octahedron from "@/components/Octahedron.vue";
</script>

<style scoped>
.initial-container {
  height: 600px;
  margin: 48px 0;
  width: 100%;
  padding: 12px;
  font-weight: bold;
}

h1 {
  font-size: 4.5rem;
}

.who-am-i {
  background: var(--darker-green);
}

.background {
  background: var(--dark-green);
}

.code-snippets {
  background: var(--green);
}

.codes a {
  color: white;
  text-decoration: none;
}

.codes a:hover {
  color: var(--light-green);
  text-decoration: none;
}

.content {
  width: 100%;
  padding: 72px 0;
}
@media screen and (max-width: 1400px) {
  h1 {
    font-size: 4rem;
  }
}

@media screen and (max-width: 1200px) {
  .image-container {
    height: 500px;
  }

  h1 {
    font-size: 3.25rem;
  }
}

@media screen and (max-width: 992px) {
  .initial-container {
    height: 500px;
    margin: 73px 0;
    justify-content: space-around!important;
    flex-direction: column!important;
  }
  
  h1 {
    font-size: 2.5rem;
  }
}

@media screen and (max-width: 768px) {
  .initial-container {
    height: 500px;
    margin: 24px 0;
  }

  h1 {
    font-size: 2.25rem;
  }
}

@media screen and (max-width: 480px) {
  h1 {
    font-size: 1.5rem;
  }

  h4 {
    font-size: 1rem;
  }

  h3 {
    font-size: 1.25rem;
  }
}
</style>
