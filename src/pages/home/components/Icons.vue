<template>
    <div class='icons'>
        <swiper :options="swiperOption">
            <swiper-slide v-for='(page,index) of pages' :key='index'>
                <div 
                    class='icon' 
                    v-for='item of page' 
                    :key='item.id'
                >
                    <div class="icon-img">
                        <img 
                            class='icon-img-content' 
                            :src='item.imgUrl'
                            alt=""
                        />
                    </div>
                    <p class='icon-desc'>热门景点</p>
                </div>                
            </swiper-slide>

        </swiper>
    </div>
</template>

<script>
    export default {

        data(){
            return{
                 swiperOption:{
                     autoplay: false
                 }
            }
        },
        props:{
            iconList:Array
        },
        computed: {
            pages(){
                let pages=[];
                this.iconList.forEach((item,index)=>{
                    const page=Math.floor(index/8);
                    if(!pages[page]){
                        pages[page]=[]
                    }
                    pages[page].push(item)
                })
                return pages;
            }
        }
    }
</script>

<style lang='stylus' scoped>
.icons
    overflow: hidden
    height: 0
    padding-bottom: 50% 
    .icon
        position: relative
        float: left
        width: 25%
        height: 0
        padding-bottom: 25% 
        .icon-img
            position: absolute
            left: 0
            right: 0
            top: 0
            bottom: .44rem // p高度
            box-sizing: border-box 
            padding .1rem
            .icon-img-content
                height: 100%
                display: block
                margin: 0 auto
        .icon-desc
            position: absolute
            left: 0
            right: 0
            bottom: 0
            height: .44rem
            line-height: .44rem
            text-align: center;
            color: $darkTextColor
</style>