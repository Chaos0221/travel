<template>
  <div>
    <home-header/>
    <home-swiper :swiperList='swiperList'/>
    <home-icons :iconList='iconList' />
    <home-recommend :recommendList='recommendList' />
    <home-weekend :weekendList='weekendList'/>
  </div>
</template>

<script>
import HomeSwiper from "./components/Swiper";
import HomeHeader from './components/Header'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
import Axios from 'axios'

export default {
  components: {
    HomeSwiper,
    HomeHeader,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  data(){
    return {
      iconList: [],
      recommendList: [],
      weekendList: [],
      swiperList: []
    }
  },
  methods:{
    getHomeInfo(){
      Axios.get('/api/index.json')
      .then(this.getHomeInfoSuc)
    },
    getHomeInfoSuc(res){
      
      this.iconList=res.data.data.iconList;
      this.recommendList=res.data.data.recommendList;
      this.weekendList=res.data.data.weekendList;
      this.swiperList=res.data.data.swiperList;

    }
  },
  mounted(){
    this.getHomeInfo()
  }
}
</script>

<style scoped>
</style>