<script setup>
  import newsList from '../assets/data/news.json';
  import NewsCard from '../components/NewsCard.vue';
</script>

<template>
  <main>
    <h1>Home - Novedades en SkullCodes</h1>

    <div class="newsList">
      <NewsCard  v-for="news in newsList" :key="news.id" :news="news" />
    </div>
  </main>
</template>

<style scoped>
</style>