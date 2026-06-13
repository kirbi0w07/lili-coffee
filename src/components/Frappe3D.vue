<template>
    <canvas ref="experience"></canvas>
</template>

<script setup lang="js">
import {PerspectiveCamera, Scene, WebGLRenderer} from 'three'
import { ref } from 'vue'

const experience = ref(null)
const scene =  new Scene()
const camera = new PerspectiveCamera(75, window.innerWidth, 0.1, 1000)
scene.add(camera)   

const renderer = new WebGLRenderer(
{
    canvas: experience.value 
}
)
renderer.setSize(window.innerWidth, window.innerHeight)
</script>

<style>

</style>