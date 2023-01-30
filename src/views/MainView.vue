<script setup>
import WavesSvg from '@/components/WavesSvg'
import StyleGuide from '@/components/StyleGuide';

</script>

<template>
  <nav>
    <RouterLink :to="{name: 'home'}"><div class="nav-item">HOME</div></RouterLink>
    <RouterLink :to="{name: 'typography'}"><div class="nav-item">COMPONENTS</div></RouterLink>
  </nav>
  <div class="main-section">
    <div class="main-title">
      <div class="float-title">gA UI</div>
    </div>
    <div class="wave-wrapper">
      <WavesSvg />
    </div>
  </div>
  <div class="style-guide">
    <StyleGuide />
  </div>
</template>

<style lang="scss" scoped>
.main-section {
  background: linear-gradient(60deg, #5178AF 0%, #9180B4 100%);
  .main-title {
    position: relative;
    font-size: 7em;
    font-weight: 900;
    color: #ffffff;
    padding-top: 200px;
    text-align: center;

    .float-title {
      position: absolute;
      top: 150px;
      left: 45%;
      animation: onWave 7s linear infinite;
    }
  }
}
#Container {
  position: relative;
  nav {
    position: absolute;
    top: 20px;
    right: 50px;
    display: flex;
    z-index: 9999;
    .nav-item {
      min-width: 80px;
      padding: 10px;
      color: #fff;
      border-radius: 2em;
      text-align: center;
      &:hover {
        background-color: rgba(255, 255, 255, 0.16);
      }
    }
  }
}
@keyframes onWave {
  0%{
    transform: translate(0, 0);
  }
  25% {
    transform: translate(-20px, 50px) rotate(5deg);
  }
  75% {
    transform: translate(10px, -30px) rotate(0deg);
  }
  100% {
    transform: translate(0, 0);
  }
}
</style>