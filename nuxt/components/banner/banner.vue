<template>
  <div v-swiper:mySwiper="swiperOption">
    <div class="swiper-wrapper">
      <div class="swiper-slide" v-for="banner in banners">
        <img :src="banner">
      </div>
    </div>
    <div class="swiper-pagination swiper-pagination-bullets"></div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        banners: [
          'http://img.vodeshop.com/201810111157350310489617.jpg?750*280',
          'http://img.vodeshop.com/201809220251290028497620.png?750*280',
          'http://img.vodeshop.com/201810010210030757150110.png?750*280'
        ],
        swiperOption: {
          loop: true,
          slidesPerView: 'auto',
          centeredSlides: true,
          autoplay:3000,
          spaceBetween: 30,
          pagination: {
            el: '.swiper-pagination',
            dynamicBullets: true
          },
          on: {
            slideChange() {
              console.log('onSlideChangeEnd', this);
            },
            tap() {
              console.log('onTap', this);
            }
          }
        },
        props: {
          loop: {
            type: Boolean,
            default: false
          }
        }
        // props: {
        //   effect: {//滚动效果
        //     type: String,
        //     default: "slide"
        //   },
        //   loop: {// 无缝
        //     type: Boolean,
        //     default: false
        //   },
        //   direction: { //图片滑动方向
        //     type: String,
        //     default: "horizontal"
        //   },
        //   paginationType: { //分页器类型
        //     type: String,
        //     default: "bullets"
        //   },
        //   autoPlay: { //轮播自动切换
        //     type: Number,
        //     default: 3000
        //   }
        // }
      }
    },

    created() {
     
    },
    mounted() {
      // this.swiperOption = {
      //   loop: true,
      //   slidesPerView: 'auto',
      //   centeredSlides: true,
      //   autoplay:3000,
      //   spaceBetween: 30,
      //   pagination: {
      //     el: '.swiper-pagination',
      //     dynamicBullets: true
      //   },
      //   on: {
      //     slideChange() {
      //       console.log('onSlideChangeEnd', this);
      //     },
      //     tap() {
      //       console.log('onTap', this);
      //     }
      //   }
      // }
      // this.mySwiper.slideTo(0)


      // this.dom = this.mySwiper("." + that.swipeid, {
      //   //循环
      //   loop: that.loop,
      //   //分页器
      //   pagination: {
      //     el: ".swiper-pagination",
      //     bulletClass: 'swiper-pagination-bullet',
      //   },
      //   //分页类型
      //   paginationType: that.paginationType,
      //   //自动播放
      //   autoPlay: that.autoPlay,
      //   //方向
      //   direction: that.direction,
      //   //特效
      //   effect: that.effect,
      //   //用户操作swiper之后，不禁止autoplay
      //   disableOnInteraction: false,
      //   //修改swiper自己或子元素时，自动初始化swiper
      //   observer: true,
      //   //修改swiper的父元素时，自动初始化swiper
      //   observeParents: true
      // });


    }
  }
</script>

<style lang="less" scoped>
  img {
    width: 100%;
  }
</style>

