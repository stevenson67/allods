<script setup>

import Hero from "@/components/hero.vue";
import Kit from "@/components/kit.vue";
</script>

<template>
  <header>
    <img src="src/assets/img/logo.png">
  </header>

  <main>
    <section class="hero">
      <img class="shadow-left" src="src/assets/img/shadow.png">
      <img class="hero_left-woman" src="src/assets/img/mafia-woman.png">
      <div class="container">
        <hero/>
      </div>
      <img class="glow" src="src/assets/img/glow.png">
      <img class="hero_right-man" src="src/assets/img/mafia-man.png">
      <img class="shadow-right" src="src/assets/img/shadow.png">
      <img class="blue-glowHero" src="src/assets/img/blue-glow2.png">
    </section>
    <section class="kit">
      <div class="container">
        <kit/>
      </div>
      <img class="blue-glow" src="src/assets/img/blue-glow.png">
    </section>
  </main>
</template>

<style lang="scss">
header {
  display: flex;
  position: absolute;
  width: 100%;
  z-index: 2;
  img {
    margin: 0 auto;
  }
}
main {
  position: relative;
  z-index: 1;
}
.hero {
  position: relative;
  overflow: hidden;
  height: 100vh;
  background-image: url("src/assets/img/hero-bg.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  .container {
    position: relative;
    z-index: 3;
  }
  &_left, &_right {
    position: relative;
    width: 30%;
    &-woman, &-man {
      position: absolute;
      bottom: 0;
      height: 100%;
      object-fit: contain;
      object-position: bottom;
    }
  }
  &_left {
    &-woman {
      left: -100px;
      z-index: 1;
      width: 35%;
    }
  }
  &_right {
    &-man {
      right: -150px;
      z-index: 1;
      width: 40%;
    }
  }
}
.kit {
  position: relative;
  overflow: hidden;
  padding-top: 54px;
  padding-bottom: 54px;
  background-image: url("src/assets/img/kit-bg.png");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.glow {
  position: absolute;
  top: 0;
  width: 2300px;
  left: 58%;
  transform: translateX(-50%);
  mix-blend-mode: screen;
  z-index: 2;
}
.blue-glow, .blue-glowHero {
  position: absolute;
  bottom: 0;
  width: 100%;
  z-index: 2;
}
.blue-glow {
  transform: revert;
}
.blue-glowHero {
  transform: rotate(180deg);
}
.shadow {
  &-left {
    position: absolute;
    left: 0; top: 0;
    z-index: 0;
  }
  &-right {
    position: absolute;
    right: 0; top: 0;
    transform: rotate(180deg);
    z-index: 0;
  }
}
</style>
