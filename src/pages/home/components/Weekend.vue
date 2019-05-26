<template>
  <div>
    <div class="title">周末去哪</div>
    <ul>
      <!-- <router-link
        tag="li"
        class="item border-bottom"
        v-for="item of list"
        :key="item.id"
      > -->
        <li        
            class="item border-bottom"
            v-for="item of list"
            :key="item.id"
        >
            <div class='item-img-wrapper'>
                <img class="item-img" src="@/assets/img/3.jpg" />
            </div>
            <div class="item-info">
                <p class="item-title">{{item.title}}</p>
                <p class="item-desc">{{item.desc}}</p>
                <button class="item-button">查看详情</button>
            </div>          
        </li>

      <!-- </router-link> -->
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  // props: {
  //   list: Array
  // },
    data(){
        return {
            list:[
                {
                  id: '001',
                  title: '一个标题',
                  desc: '一段描述'
                },
                                {
                  id: '002',
                  title: '一个标题',
                  desc: '一段描述'
                },
                                {
                  id: '003',
                  title: '一个标题',
                  desc: '一段描述'
                },
                                {
                  id: '004',
                  title: '一个标题',
                  desc: '一段描述'
                },
            ]
        }
    }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 37.09%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()
    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()
</style>
