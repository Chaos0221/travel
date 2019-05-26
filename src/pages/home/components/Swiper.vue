<template>
<div class='wrapper'>
  <swiper :options="swiperOption">
    <!-- <swiper-slide v-for="item in swiperList" :key='item.id'>
      <img :src="item.imgUrl" alt=''/>
    </swiper-slide> -->
    <swiper-slide>
      <img src="@/assets/img/1.jpg" alt="" class='swiper-img'>
    </swiper-slide>
        <swiper-slide>
      <img src="@/assets/img/2.jpg" alt="" class='swiper-img'>
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>  
test
</div>

</template>

<script>
export default {
  name: "carousel",
  data() {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList:[
        {
          id:'0001',
          imgUrl: '@/assets/img/1.jpg'
        },
        {
          id:'0002',
          imgUrl: '@/assets/img/2.jpg'
        }
      ]
    };
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
    padding-bottom: 42.67%  
    // padding的百分比相对width 实现图片比例自适应
    background: #eee
    .swiper-img
      width: 100%
</style>