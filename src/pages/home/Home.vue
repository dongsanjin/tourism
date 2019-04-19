<template>
  <div class="wrapper">
    <home-header></home-header>
    <home-swiper :list="swiperList"></home-swiper>
    <home-icons :list="iconList"></home-icons>
    <home-list :scrollItem="scrollItem"></home-list>
    <home-link :linkList="linkList"></home-link>
    <home-weekend></home-weekend>
  </div>
</template>
<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeWeekend from './components/Weekend'
import HomeList from './components/List'
import HomeLink from './components/Link'
import axios from 'axios'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeList,
    HomeLink,
    HomeWeekend
  },
  data () {
    return {
      swiperList: [],
      iconList: [],
      scrollItem: [],
      linkList: []
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.scrollItem = data.scrollItem
        this.linkList = data.linkList
      }
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper
    background-color #f5f5f5
</style>
