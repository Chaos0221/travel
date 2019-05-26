<template>
  <div>
    <home-header/>
    <home-swiper/>
    <home-icons/>
  </div>
</template>

<script>
import HomeSwiper from "./components/Swiper";
import HomeHeader from './components/Header'
import HomeIcons from './components/Icons'

export default {
  components: {
    HomeSwiper,
    HomeHeader,
    HomeIcons
  }
}
</script>

<style scoped>
</style>