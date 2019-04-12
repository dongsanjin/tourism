<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/eb47a432471be6ac40b69828676479dd.jpg_750x200_207de9c6.jpg'
      },
      {
        id: '0002',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/f8675864efa49385315a488009f7028a.jpg_750x200_52b0d4bf.jpg'
      }]
    }
  }
}
</script>
<style scoped lang="stylus">
  .wrapper >>> .swiper-pagination-bullet-active
    background #fff
  .wrapper
    width 100%
    height 0
    overflow hidden
    padding-bottom 26.75%
    background-color #eee
    .swiper-img
      width: 100%;
</style>
