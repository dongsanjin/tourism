<template>
  <div class="header">
    <router-link tag="div" to="/" class="back-header iconfont" v-if="showBack">&#xe624;</router-link>
    <div class="wrapper" v-if="showHeader" :style="opacityShow">
      <router-link tag="span" to="/" class="iconfont back-index">&#xe624;</router-link>
      云雾山
    </div>
  </div>
</template>
<script>
export default {
  name: 'Header',
  data () {
    return {
      showBack: true,
      showHeader: false,
      opacityShow: {
        opacity: 0
      }
    }
  },
  methods: {
    handleScroll () {
      let top = document.documentElement.scrollTop
      if (top > 10) {
        let opacity = top / 180
        opacity = opacity >= 1 ? 1 : opacity
        this.opacityShow = { opacity }
        this.showBack = false
        this.showHeader = true
      } else {
        this.showBack = true
        this.showHeader = false
      }
    }
  },
  activated () {
    window.addEventListener('scroll', this.handleScroll)
  },
  deactivated () {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .back-header
    position absolute
    top .2rem
    left .2rem
    width .6rem
    height .6rem
    line-height .6rem
    border-radius .3rem
    color #fff
    text-align center
    font-weight bold
    background-color rgba(0,0,0,.5)
  .wrapper
    z-index 99
    position fixed
    top 0
    left 0
    right 0
    height $headerHeight
    line-height $headerHeight
    background-color $bgColor
    text-align center
    color #fff
    font-size .32rem
    .back-index
      position absolute
      left .2rem
      font-size .36rem
      font-weight bold
</style>
