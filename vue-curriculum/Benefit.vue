<template>
  <section class="p-benefit">
    <div class="p-benefit__inner l-inner">
      <div class="p-benefit__items">
        <div class="p-benefit__item" v-for="(benefit, index) in benefits" :key="index">
          <div class="p-benefit__img">
            <img :src="benefit.image" :alt="benefit.alt" />
          </div>
          <div class="p-benefit__body">
            <h3 class="p-benefit__title">{{ benefit.title }}</h3>
            <p class="p-benefit__text" v-html="benefit.text"></p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import benefitImage1 from '@/assets/images/benefit-1.png'
import benefitImage2 from '@/assets/images/benefit-2.png'
import benefitImage3 from '@/assets/images/benefit-3.png'

const benefits = [
  {
    image: benefitImage1,
    alt: "未経験でも安心",
    title: "未経験でも安心",
    text: "東京ITスクールでは、<br>未経験者でもわかりやすく学べるカリキュラムをご用意しています。"
  },
  {
    image: benefitImage2,
    alt: "実践的なスキルが身に付く",
    title: "実践的なスキルが身に付く",
    text: "現場で活躍する講師による実践的な授業で、<br>即戦力となるスキルを習得できます。"
  },
  {
    image: benefitImage3,
    alt: "就職・転職サポートが充実",
    title: "就職・転職サポートが充実",
    text: "キャリアアドバイザーが、<br>あなたの就職・転職をしっかりとサポートします。"
  }
]
</script>

<style scoped>
</style>
