<template>
  <section class="p-service">
    <div class="p-service__inner l-inner">
      <h2 class="p-service__title">サービス</h2>
      <div class="p-service__list">
        <div
          class="p-service__item"
          v-for="(service, index) in serviceList"
          :key="index"
        >
          <div class="p-service__icon">
            <img :src="service.icon" :alt="service.name" />
          </div>
          <div class="p-service__info">
            <h3 class="p-service__name">{{ service.name }}</h3>
            <p class="p-service__description">{{ service.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import sampleImage1 from '@/assets/images/image-1.png'
import sampleImage2 from '@/assets/images/image-2.png'
const serviceList = [
  {
    name: "Web Development",
    description: "最新のウェブ技術を駆使して、魅力的で機能的なウェブサイトを作成します。",
    icon: sampleImage1
  },
  {
    name: "Mobile App Development",
    description: "スマートフォン向けのアプリケーション開発を行います。",
    icon: sampleImage2
  },
  {
    name: "SEO Optimization",
    description: "検索エンジン最適化を通じて、サイトのアクセス数を向上させます。",
    icon: sampleImage1
  }
];
</script>

<style scoped>
.p-service__list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.p-service__item {
  background-color: #fff;
  border: 1px solid #ddd;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  text-align: center;
}

.p-service__icon img {
  width: 80px;
  height: 80px;
  object-fit: contain;
  margin-bottom: 1rem;
}

.p-service__name {
  font-size: 1.25rem;
  font-weight: bold;
  color: #333;
  margin-bottom: 0.5rem;
}

.p-service__description {
  color: #666;
  font-size: 0.95rem;
}
</style>
