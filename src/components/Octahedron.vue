<template>
  <canvas id="canvas" width="300" height="300"></canvas>
</template>

<script lang="ts" setup>
import { onMounted } from "vue";
import * as THREE from 'three';
import { OrbitControls } from 'three/examples/jsm/controls/OrbitControls';


const scene = new THREE.Scene();
scene.background = new THREE.Color('#272727')

const camera = new THREE.PerspectiveCamera(75, 1, 0.1, 1000);
camera.position.set(2, 2, 10);

let renderer: THREE.WebGLRenderer;
let controls: OrbitControls;

const geometry = new THREE.OctahedronGeometry(5, 0);
const material = new THREE.MeshStandardMaterial({color: '#17592E'});
const octahedron = new THREE.Mesh(geometry,  material);
const line = new THREE.Line( geometry, new THREE.MeshStandardMaterial( {color: '#fff'}));
scene.add(octahedron, line);

const pointLight = new THREE.PointLight('#fff', 5, 100);
pointLight.position.set(40, 40, 40);

const ambientLight = new THREE.AmbientLight('#fff')
scene.add(pointLight, ambientLight);

function animate() {
  requestAnimationFrame(animate);

  octahedron.rotation.x += 0.01
  octahedron.rotation.y += 0.005
  octahedron.rotation.z += 0.01

  line.rotation.x += 0.01
  line.rotation.y += 0.005
  line.rotation.z += 0.01

  controls.update();
  renderer.render(scene, camera);
}

onMounted(() => {
  renderer = new THREE.WebGLRenderer({canvas: document.querySelector('#canvas') as HTMLCanvasElement})
  renderer.render(scene, camera);

  controls = new OrbitControls(camera, renderer.domElement)
  animate()
})
</script>
