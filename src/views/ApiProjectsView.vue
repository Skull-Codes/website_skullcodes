<script setup>
  import apiProjects from '../assets/data/api_projects.json';
  import Card from '../components/Card.vue';
  const techs = [
    "Estructura básica con patrón MVC, Router, conexión a base de datos, Servir archivos y Variables de entorno", 
    "Implementación de Autenticación JWT", 
    "Contenedores Docker y Compose, Test unitarios, Linter e Integración con Git CI_CD", 
    "Documentación de código con Swagger"];

  const projects = apiProjects.reverse();
    
</script>

<template>
  <div class="api">
    <h1>Projectos API</h1>
    <h3>Projectos preparados con las siguientes caracteristicas:</h3>
    <ul>
      <li v-for="(tech, index) in techs" :key="index">
        {{ tech }}
      </li>
    </ul>

    <br/>

    <div class="cardlist">
      <Card  v-for="project in projects" :key="project.id" :project="project" />
    </div>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .api {
    min-height: 100vh;
        display: flex;
        align-items: left;
        flex-direction: column;
        justify-content: center;
  }
}
</style>
