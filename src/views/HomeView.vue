<script setup>
  import newsData from '../assets/data/news_data.json';
  import NewsCard from '../components/NewsCard.vue';

  const newsList = newsData.reverse();
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