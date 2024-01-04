<script setup>
// import Data from '../Json.js/proyectos.js'
defineProps(['projectName', 'projectDescription', 'buttonText', 'projectLink'])
</script>

<template>
  <div class="card" style="width: 18rem">
    <div class="card-body row">
      <h5 class="card-title row justify-content-center">{{ projectName }}</h5>
      <p class="card-text">{{ projectDescription }}</p>
      <a :href="projectLink" target="_blank" class="btn btn-primary justify-content-center">{{
        buttonText
      }}</a>
    </div>
  </div>
</template>
