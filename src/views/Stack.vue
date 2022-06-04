<template>
  <div class="stack-page py-5">
    <div class="container">
      <div class="stack">
        <div class="py-5 appear-animation">
          <h3>My Stack</h3>
          <h1>Web Curriculum</h1>
          <h4>Technologies that I know</h4>
        </div>

        <div class="py-4 appear-animation opacity d-flex flex-column justify-content-center">
          <h2 class="py-4">Vue.js</h2>
          <div class="grid vue">
            <div class="py-2 px-4">
              <img class="img-size-48" src="@/assets/logo.png" alt="vue logo" />
              <h2>Vue 2</h2>
              <p>
                I first tarted working with vue 2, it's a really good framework and easy to learn 
              </p>
            </div>

            <div class="py-2 px-4">
              <img class="img-size-48" src="@/assets/logo.png" alt="vue logo" />
              <h2>Vue 3</h2>
              <p>
                Vue 3 is my main framework today, the composition API is powerful and simple.
              </p>
            </div>

            <div class="py-2 px-4">
              <img
                class="img-size-48"
                src="@/assets/vuex.png"
                alt="vuex logo"
              />
              <h2>Vuex</h2>
              <p>Good state manager, I used it a lot before knowing Pinia</p>
            </div>

            <div class="py-2 px-4">
              <img
                class="img-size-48"
                src="@/assets/pinia.svg"
                alt="pinia logo"
              />
              <h2>Pinia</h2>
              <p>My favorite state manager. Easy to learn and to reuse code, life could be a dream</p>
            </div>

            <div class="py-2 px-4">
              <img
                class="img-size-48"
                src="@/assets/vue_router.png"
                alt="pinia logo"
              />
              <h2>Vue Router</h2>
              <p>Simple and useful way to navigate through the pages</p>
            </div>
          </div>
        </div>

        <div class="py-4 appear-animation opacity" style="animation-delay: 1s;">
          <h2 class="py-4">JavaScript</h2>
          <div class="grid javascript">
            <div class="py-2 px-4">
              <img
                class="img-size-48"
                src="@/assets/typescript_logo.png"
                alt="typescript logo"
              />
              <h2>TypeScript</h2>
              <p>Started using in early 2022, it is a nice way to make more robust JavaScript code</p>
            </div>

            <div class="py-2 px-4">
              <img
                class="img-size-48"
                style="background: white; border-radius: 6px;"
                src="@/assets/three.png"
                alt="three.js logo"
              />
              <h2>Three.js</h2>
              <p>Great Framework to create 3D canvas, the crystal in the home page was written with three.js</p>
            </div>

            <div class="py-2 px-4">
              <img
                class="img-size-48"
                src="@/assets/chartjs.png"
                alt="chart.js logo"
              />
              <h2>Chart.js</h2>
              <p>Simple library to make beatiful charts, I used it a lot in 2021</p>
            </div>
          </div>
        </div>

        <div class="py-4 appear-animation opacity" style="animation-delay: 2s;">
          <h2 class="py-4">Python</h2>
          <div class="grid python">
            <div class="py-2 px-4">
              <img
                class="img-size-48"
                src="@/assets/django.jpg"
                alt="django logo"
              />
              <h2>django</h2>
              <p>Really good web framework, I've been working with django since 2021</p>
            </div>

            <div class="py-2 px-4">
              <img
                class="img-size-48"
                src="@/assets/fastapi.svg"
                alt="fastapi logo"
              />
              <h2>FastAPI</h2>
              <p>Simples and clean web framework, I started learning in 2022</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
h1 {
  font-size: 3rem;
  font-weight: bold;
}

.img-size-48 {
  height: 48px;
  width: 48px;
}

.grid {
  display: grid;
  grid-template-columns: 16.66% 16.66% 16.66% 16.66% 16.66% 16.66%;
}
.vue div:nth-child(1) {grid-column: 1 / span 2;}
.vue div:nth-child(2) {grid-column: 3 / span 2;}
.vue div:nth-child(3) {grid-column: 5 / span 2;}
.vue div:nth-child(4) {grid-column: 1 / span 3;}
.vue div:nth-child(5) {grid-column: 4 / span 3;}
.javascript div:nth-child(1) {grid-column: 1 / span 2;}
.javascript div:nth-child(2) {grid-column: 3 / span 2;}
.javascript div:nth-child(3) {grid-column: 5 / span 2;}
.python div:nth-child(1) {grid-column: 1 / span 3;}
.python div:nth-child(2) {grid-column: 4 / span 3;}

@media screen and (max-width: 768px) {
  .vue div:nth-child(1) {grid-column: 1 / span 3;}
  .vue div:nth-child(2) {grid-column: 4 / span 3;}
  .vue div:nth-child(3) {grid-column: 1 / span 3;}
  .vue div:nth-child(4) {grid-column: 4 / span 3;}
  .vue div:nth-child(5) {grid-column: 1 / span 6;}
  .javascript div:nth-child(1) {grid-column: 1 / span 3;}
  .javascript div:nth-child(2) {grid-column: 4 / span 3;}
  .javascript div:nth-child(3) {grid-column: 1 / span 6;}
  .python div:nth-child(1) {grid-column: 1 / span 3;}
  .python div:nth-child(2) {grid-column: 4 / span 3;}
}

@media screen and (max-width: 480px) {
  h1 {
    font-size: 2.245rem;
  }

  .vue div:nth-child(1) {grid-column: 1 / span 6;}
  .vue div:nth-child(2) {grid-column: 1 / span 6;}
  .vue div:nth-child(3) {grid-column: 1 / span 6;}
  .vue div:nth-child(4) {grid-column: 1 / span 6;}
  .vue div:nth-child(5) {grid-column: 1 / span 6;}
  .javascript div:nth-child(1) {grid-column: 1 / span 6;}
  .javascript div:nth-child(2) {grid-column: 1 / span 6;}
  .javascript div:nth-child(3) {grid-column: 1 / span 6;}
  .python div:nth-child(1) {grid-column: 1 / span 6;}
  .python div:nth-child(2) {grid-column: 1 / span 6;}
}
</style>
