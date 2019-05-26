<template>
  <div>
    <home-header/>
    <home-swiper/>
    <home-icons/>
    <home-recommend/>
    <home-weekend/>
  </div>
</template>

<script>
import HomeSwiper from "./components/Swiper";
import HomeHeader from './components/Header'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'


export default {
  components: {
    HomeSwiper,
    HomeHeader,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  }
}
</script>

<style scoped>
</style>