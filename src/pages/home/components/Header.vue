<template>
  <div class="header">
    <div class="header-left">
        <div class='iconfont back-icon'>&#xe624;</div>
    </div>
    <div class="header-input">
        <span class="iconfont">&#xe632;</span>
        输入城市/景点/主题
    </div>
    <div class="header-right">
        <span class="iconfont">&#xe64a;</span>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.styl'

.header
    display: flex
    line-height: .86rem
    background: $bgColor
    color: #fff
    .header-left
        width: .64rem
        float: left 
        .back-icon
            text-align: center
            font-size: .4rem
    .header-input
        margin-top: .12rem
        margin-left: .2rem
        border-radius: .1rem
        line-height: .64rem
        height: .64rem
        flex: 1
        background:#fff
        color:#ccc
    .header-right
        float: right
        width: 1.24rem
        text-align: center

</style>