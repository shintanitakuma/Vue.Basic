<template>
  <section class="p-news">
    <div class="p-news__inner l-inner">
      <h2 class="p-news__title">お知らせ</h2>
      <ul class="p-news__list">
        <li class="p-news__item" v-for="(news, index) in newsList" :key="index">
          <span class="p-news__date">{{ news.date }}</span>
          <span class="p-news__category" :class="`is-${news.category.toLowerCase()}`">
            {{ news.category }}
          </span>
          <span class="p-news__title">{{ news.title }}</span>
        </li>
      </ul>
    </div>
  </section>
</template>

<script setup>
const newsList = [
  { date: "2025.04.01", category: "News", title: "新しいコースを開始しました！" },
  { date: "2025.03.20", category: "Media", title: "メディア掲載のお知らせ" },
  { date: "2025.03.10", category: "Blog", title: "春期講習レポートを公開しました" }
];
</script>

<style scoped>
.p-news__list {
  margin-top: 2rem;
}

.p-news__item {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 1px solid #ddd;
  font-size: 0.95rem;
}

.p-news__date {
  color: #666;
  width: 100px;
  flex-shrink: 0;
}

.p-news__category {
  padding: 0.2em 0.6em;
  border-radius: 4px;
  font-size: 0.75rem;
  color: #fff;
  flex-shrink: 0;
}

.is-news {
  background-color: #007bff;
}
.is-media {
  background-color: #28a745;
}
.is-blog {
  background-color: #ffc107;
}

.p-news__title {
  flex: 1;
}
</style>