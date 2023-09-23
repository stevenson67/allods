<template>
  <div class="hero-wrap">
    <div class="hero_left"></div>
    <div class="hero_boxes">
      <img class="hero_boxes-box" src="src/assets/img/boxes.png">
      <h1 class="hero_boxes-title">КОЛЛЕКЦИОННЫЕ ИЗДАНИЯ</h1>
      <p class="hero_boxes-desc">Побеждайте легко, побеждайте стильно с новыми коллекционными изданиями «Аллодов Онлайн»!</p>
    </div>
    <div class="hero_right"></div>
  </div>
</template>

<script>
export default {
  name: "hero"
}
</script>

<style lang="scss">
.hero {
  &-wrap {
    position: relative;
    display: flex;
    justify-content: space-between;
    height: 100%;
  }
  &_boxes {
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: center;
    padding-bottom: 50px;
    position: relative;
    text-align: center;
    z-index: 3;
    width: 65%;
    &-box {
      position: absolute;
      top: 55%;
      transform: translateY(-50%);
      width: 100%;
    }
    &-title {
      font-size: 42px;
      font-weight: 700;
      line-height: 49px;
      margin-bottom: 25px;
    }
    &-desc {
      font-size: 20px;
      font-weight: 400;
      line-height: 23px;
    }
  }
}
</style>