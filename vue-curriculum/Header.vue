<template>
  <header class="l-header">
    <div class="l-header__title">
      <img class="l-header__img" :src="sampleImage" alt="ヘッダーの画像" />
      <h2 class="l-header__heading">カリキュラム</h2>
    </div>
    <div class="l-header__list">
      <nav>
        <ul class="l-header__group">
          <li class="l-header__item"><a class="l-header__link" href="//〇〇〇〇〇〇〇〇〇.com/">message</a></li>
          <li class="l-header__item"><a class="l-header__link" href="https://〇〇〇〇〇〇〇〇〇.com/">p-service</a></li>
          <li class="l-header__item"><a class="l-header__link" href="https://〇〇〇〇〇〇〇〇〇.com/">member</a></li>
          <li class="l-header__item"><a class="l-header__link" href="https://〇〇〇〇〇〇〇〇〇.com/">benefit</a></li>
          <li class="l-header__item"><a class="l-header__link" href="https://〇〇〇〇〇〇〇〇〇.com/">contact</a></li>
        </ul>
      </nav>
      <div class="l-header__burgers" @click="toggleMenu">
        <div class="l-header__burger">
          <div class="l-header__burgerList"></div>
          <div class="l-header__burgerList"></div>
          <div class="l-header__burgerList"></div>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
import sampleImage from '@/assets/images/logo.png'
import { ref } from 'vue'

const toggleMenu = () => {
  console.log("バーガーメニューがクリックされました");
}
</script>

<style scoped>
</style>
