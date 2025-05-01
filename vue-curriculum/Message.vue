<template>
  <section class="p-message">
    <div class="p-message__inner l-inner">
      <h2 class="p-message__title">代表メッセージ</h2>
      <div class="p-message__content">
        <div class="p-message__image">
          <img src="https://placehold.jp/200x200.png" alt="代表の写真" />
        </div>
        <div class="p-message__text">
          <p class="p-message__comment">
            私たちは「すべての人に、プログラミングの楽しさを」をモットーに、誰もがITスキルを身につけられる学習環境を提供しています。<br />
            初心者の方でも安心して学べるよう、丁寧なサポート体制を整えています。<br />
            一歩踏み出す勇気を、私たちが全力で応援します！
          </p>
          <p class="p-message__name">代表取締役 山田 太郎</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.p-message__content {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 2rem;
  margin-top: 2rem;
}

.p-message__image img {
  width: 200px;
  height: 200px;
  object-fit: cover;
  border-radius: 50%;
}

.p-message__text {
  flex: 1;
}

.p-message__comment {
  font-size: 1rem;
  line-height: 1.8;
  margin-bottom: 1rem;
}

.p-message__name {
  font-weight: bold;
  font-size: 1.1rem;
  text-align: right;
}
</style>