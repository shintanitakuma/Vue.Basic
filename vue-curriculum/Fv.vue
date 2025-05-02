<script setup>
import sampleImage1 from '@/assets/images/sample-1.jpeg'
import sampleImage2 from '@/assets/images/sample-2.jpeg'
</script>

<template>
  <section class="p-fv">
    <div class="p-fv__title">
      <h2 class="p-fv__heading">
        入門カリキュラム<br />HTML・CSS
      </h2>
      <p class="p-fv__text">
        入門カリキュラムHTML・CSSの 最終課題LPです。これができれば入門カリキュラム
        <br class="p-fv__space" />HTML・CSSは終了です。
      </p>
    </div>
    <img class="p-fv__img" :src="sampleImage1" alt="Cat" />
  </section>
</template>
