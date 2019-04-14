<template>
  <div>
    <div class="area area-city">
      <div class="area-title">
        热门城市
      </div>
      <ul class="area-list-wrapper">
        <li class="area-list">北京</li>
        <li class="area-list">上海</li>
        <li class="area-list">三亚</li>
        <li class="area-list">香港</li>
        <li class="area-list">杭州</li>
        <li class="area-list">广州</li>
        <li class="area-list">成都</li>
        <li class="area-list">深圳</li>
        <li class="area-list">苏州</li>
        <li class="area-list">桂林</li>
        <li class="area-list">西安</li>
        <li class="area-list">厦门</li>
      </ul>
    </div>
    <div class="area area-letter">
      <div class="area-title">
        字母排序
      </div>
      <ul class="letter-list-wrapper">
        <li class="letter-list">A</li>
        <li class="letter-list">B</li>
        <li class="letter-list">C</li>
        <li class="letter-list">D</li>
        <li class="letter-list">E</li>
        <li class="letter-list">F</li>
        <li class="letter-list">G</li>
        <li class="letter-list">H</li>
        <li class="letter-list">J</li>
        <li class="letter-list">K</li>
        <li class="letter-list">L</li>
        <li class="letter-list">M</li>
        <li class="letter-list">N</li>
        <li class="letter-list">P</li>
        <li class="letter-list">Q</li>
        <li class="letter-list">R</li>
        <li class="letter-list">S</li>
        <li class="letter-list">T</li>
        <li class="letter-list">W</li>
        <li class="letter-list">X</li>
        <li class="letter-list">Y</li>
        <li class="letter-list">Z</li>
      </ul>
    </div>
    <div class="area area-mroe">
      <div class="area-title">
        A
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'CityList'
}
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .area-title
    text-indent $titleIndent
    height .8rem
    line-height .8rem
    font-size .2rem
    background #F5F5F5
  .area-list-wrapper
    position relative
    display flex
    flex-flow row wrap
    overflow hidden
    &:before
      content: ''
      position absolute
      left 33.3%
      width 33.3%
      height 100%
      border-left .02rem solid #DDDDDD
      border-right .02rem solid #DDDDDD
    .area-list
      flex 33.3%
      text-align center
      height .9rem
      line-height .9rem
      border-bottom 0.02rem solid #DDDDDD
      margin-bottom -1px
  .letter-list-wrapper
    padding  .3rem 0
    overflow hidden
    .letter-list
      width 16.6%
      height 1rem
      line-height 1rem
      float left
      font-size .3rem
      text-align center
      text-indent 0
  .area-mroe
    &::before
      content ''
      display block
      width 0
      clear both
</style>
