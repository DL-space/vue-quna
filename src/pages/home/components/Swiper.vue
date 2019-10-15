<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
      <!-- <div class="swiper-button-prev" slot="button-prev"></div>
      <div class="swiper-button-next" slot="button-next"></div> -->
      <!-- <div class="swiper-scrollbar" slot="scrollbar"></div> -->
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination'
      },
      swiperList: [
        {
          id: 1,
          imgUrl: 'https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=414714612,3578024566&fm=26&gp=0.jpg'
        },
        {
          id: 2,
          imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1571129454014&di=56ae06f9f10de6843e116c9204b56f4b&imgtype=0&src=http%3A%2F%2F08imgmini.eastday.com%2Fmobile%2F20180922%2F20180922185447_4ebb855103df05d8ea3c5095f2c46d4b_6.jpeg'
        },
        {
          id: 3,
          imgUrl: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1571129454015&di=138f5c1e5ef2ab32b748b7b3cf06e605&imgtype=0&src=http%3A%2F%2Fdik.img.kttpdq.com%2Fpic%2F104%2F72130%2F642d35a28f2a305d_1366x768.jpeg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper
    overflow hidden
    width 100%
    background #eee
    .swiper-img
      width 100%
      height 2.4rem
</style>
