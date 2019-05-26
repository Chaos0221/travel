<template>
<div class='wrapper'>
  <swiper :options="swiperOption" v-if='showSwiper'>
    <swiper-slide v-for="item in swiperList" :key='item.id'>
      <img 
        :src="item.imgUrl" 
        alt=''  
        class='swiper-img'
      />
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>  
</div>

</template>

<script>
export default {
  name: "carousel",
  data() {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay:3000
      }
    };
  },
  props:{
    swiperList: Array
  },
  computed:{
    showSwiper(){
      return this.swiperList.length
    }
  }
};
</script>

<style lang='stylus' scoped>
  // 让wrapper内的所有后代的.swiper...类生效
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 31.25%  
    // padding的百分比相对width 实现图片比例自适应
    background: #eee
    .swiper-img
      width: 100%
</style>