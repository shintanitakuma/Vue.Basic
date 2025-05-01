<template>
  <section class="p-members">
    <div class="p-members__inner l-inner">
      <h2 class="p-members__title">講師紹介</h2>
      <ul class="p-members__list">
        <li class="p-members__item" v-for="(member, index) in members" :key="index">
          <div class="p-members__image">
            <img :src="member.image" :alt="member.name" />
          </div>
          <div class="p-members__info">
            <h3 class="p-members__name">{{ member.name }}</h3>
            <p class="p-members__role">{{ member.role }}</p>
            <p class="p-members__comment">{{ member.comment }}</p>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>

<script setup>
import sampleImage from '@/assets/images/member-bg.png'
const members = [
  {
    name: "山田 太郎",
    role: "フロントエンド講師",
    comment: "初心者の方でも丁寧にサポートします！",
    image: "https://placehold.jp/150x150.png"
  },
  {
    name: "佐藤 花子",
    role: "バックエンド講師",
    comment: "一緒に楽しく学んでいきましょう！",
    image: "https://placehold.jp/150x150.png"
  },
  {
    name: "田中 一郎",
    role: "キャリアアドバイザー",
    comment: "就職・転職の相談もお任せください！",
    image: "https://placehold.jp/150x150.png"
  }
];
</script>

<style scoped>
.p-members__list {
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
  margin-top: 2rem;
}

.p-members__item {
  width: calc(33.333% - 1.333rem);
  background: #f9f9f9;
  border-radius: 8px;
  padding: 1rem;
  text-align: center;
}

.p-members__image img {
  border-radius: 50%;
  width: 100px;
  height: 100px;
  object-fit: cover;
}

.p-members__name {
  margin-top: 1rem;
  font-size: 1.2rem;
  font-weight: bold;
}

.p-members__role {
  color: #666;
  font-size: 0.9rem;
}

.p-members__comment {
  margin-top: 0.5rem;
  font-size: 0.95rem;
}
</style>