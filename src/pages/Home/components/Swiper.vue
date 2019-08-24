<template>
  <div class="swiper-container">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(item, index) of ImgUrlList" :key="index">
        <img class="swiper-img" :src="item" alt />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  components: {},
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination'
        },
        autoplay: true
      },
      ImgUrlList: [
        'static/images/banner1.jpg',
        'static/images/banner2.jpg',
        'static/images/banner3.jpg'
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.swiper-container >>>.swiper-pagination-bullet-active
    background: #fff;
.swiper-container {
    width: 100%;
    height: 31.25vw;
    background: #eee;
    .swiper-img {
        width: 100%;
    }
}
</style>
