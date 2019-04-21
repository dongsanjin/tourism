<template>
  <div>
    <div class="wrapper">
      <ul>
        <li class="img-box" v-for="item of imgList" :key="item.id" @click="handleShowAlbum">
          <img class="img-list" :src="item.imgUrl">
        </li>
      </ul>
    </div>
    <div class="album" v-if="showAlbum" @click="changeShowAlbum">
      <div class="img-wrapper">
        <swiper :options="swiperOptions" class="album-box">
          <swiper-slide v-for="(item, index) of imgItem" :key="index">
            <img class="img-item" :src="item.imgUrl">
          </swiper-slide>
          <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'List',
  data () {
    return {
      showAlbum: false,
      swiperOptions: {
        pagination: '.swiper-pagination',
        paginationType: 'fraction'
      },
      imgList: [
        {
          id: '01',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1501/10/1012e4a2c398409c.water.jpg_350x240_56977146.jpg'
        },
        {
          id: '02',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1501/28/28448e2530c6a150.water.jpg_350x240_75a7387f.jpg'
        },
        {
          id: '03',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/21/213a39d0d75b2da4.water.jpg_350x240_c1691a47.jpg'
        },
        {
          id: '04',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/d7/d7b8b72d655661f0.water.jpg_350x240_3961c73d.jpg'
        },
        {
          id: '05',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/50/5072da8b4481c9bc.water.jpg_350x240_49470b28.jpg'
        },
        {
          id: '06',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1501/6d/6d77cc467299dad7.water.jpg_350x240_9d7a08dc.jpg'
        },
        {
          id: '07',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/47/479aa2f86136854c.water.jpg_350x240_bc4a74c1.jpg'
        },
        {
          id: '08',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/33/338e44160709bf7f.water.jpg_350x240_fca8ac44.jpg'
        },
        {
          id: '09',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/ae/ae3dd9907bfcf837.water.jpg_350x240_de8bd6c7.jpg'
        },
        {
          id: '10',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/3e/3e320438fcd897c8.water.jpg_350x240_59b42425.jpg'
        },
        {
          id: '11',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/cf/cf4e19dfa7fdc7c9.water.jpg_350x240_8cffcffa.jpg'
        },
        {
          id: '12',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/ae/ae3dd9907bfcf837.water.jpg_350x240_de8bd6c7.jpg'
        },
        {
          id: '13',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/5b/5b4eef2e3b2a2811.water.jpg_350x240_a7538fd1.jpg'
        }
      ],
      imgItem: [
        {
          id: '01',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1501/10/1012e4a2c398409c.water.jpg_r_800x800_1cd8b126.jpg'
        },
        {
          id: '02',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1501/28/28448e2530c6a150.water.jpg_r_800x800_e17c3a04.jpg'
        },
        {
          id: '03',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/21/213a39d0d75b2da4.water.jpg_r_800x800_f3400f26.jpg'
        },
        {
          id: '04',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/d7/d7b8b72d655661f0.water.jpg_r_800x800_041c53f2.jpg'
        },
        {
          id: '05',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/50/5072da8b4481c9bc.water.jpg_r_800x800_aa357bb7.jpg'
        },
        {
          id: '06',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1501/6d/6d77cc467299dad7.water.jpg_r_800x800_4a71d973.jpg'
        },
        {
          id: '07',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/47/479aa2f86136854c.water.jpg_r_800x800_9a6b6d39.jpg'
        },
        {
          id: '08',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/33/338e44160709bf7f.water.jpg_r_800x800_6bda3f2c.jpg'
        },
        {
          id: '09',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/ae/ae3dd9907bfcf837.water.jpg_r_800x800_55a8eab7.jpg'
        },
        {
          id: '10',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/3e/3e320438fcd897c8.water.jpg_r_800x800_ffc73400.jpg'
        },
        {
          id: '11',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/cf/cf4e19dfa7fdc7c9.water.jpg_r_800x800_b8551938.jpg'
        },
        {
          id: '12',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/ae/ae3dd9907bfcf837.water.jpg_r_800x800_55a8eab7.jpg'
        },
        {
          id: '13',
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1503/5b/5b4eef2e3b2a2811.water.jpg_r_800x800_a1e816b8.jpg'
        }
      ]
    }
  },
  methods: {
    handleShowAlbum () {
      this.showAlbum = true
    },
    changeShowAlbum () {
      this.showAlbum = false
    }
  }
}
</script>
<style lang="stylus" scoped>
  .album >>> .swiper-container
    overflow inherit
  .wrapper
    margin-top 1rem
    background-color #F5F5F5
    padding .2rem
    .img-box
      width 50%
      float left
      box-sizing border-box
      margin-bottom .1rem
      &:nth-child(odd)
        padding-right .05rem
      &:nth-child(even)
        padding-left .05rem
      .img-list
        width 100%
        max-width 100%
  .album
    position fixed
    top 0
    right 0
    bottom 0
    left 0
    display flex
    flex-direction column
    justify-content center
    background-color black
    .album-box
      display flex
      flex-direction column
      justify-content center
      .swiper-pagination
        color #fff
        bottom -3.8rem
    .img-item
      max-width 100%
</style>
