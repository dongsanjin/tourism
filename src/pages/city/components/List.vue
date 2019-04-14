<template>
  <div>
    <div v-if="selected">
      <div class="area popular-city">
        <div class="area-title">
          {{popularCity}}
        </div>
        <ul class="popular-list-wrapper">
          <li class="popular-list" v-for="item of popularCityList" :key="item.id">{{item.listName}}</li>
        </ul>
      </div>
      <div class="area area-letter">
        <div class="area-title">
          {{letterSort}}
        </div>
        <ul class="letter-list-wrapper">
          <li class="letter-list" v-for="item of letterList" :key="item.id">{{item.letterName}}</li>
        </ul>
      </div>
      <div class="area all-city" v-for="item of allCityList" :key="item.id">
        <div class="area-title">
          {{item.title}}
        </div>
        <ul class="all-city-list-wrapper">
          <li class="all-list" v-for="list of item.cityList" :key="list.id">{{list.cityName}}</li>
        </ul>
      </div>
    </div>
    <div v-else>
      <div class="area popular-city">
        <div class="area-title">
          {{popularCity}}
        </div>
        <ul class="popular-list-wrapper">
          <li class="popular-list" v-for="item of outerPopularCityList" :key="item.id">{{item.listName}}</li>
        </ul>
      </div>
      <div class="area area-letter">
        <div class="area-title">
          {{letterSort}}
        </div>
        <ul class="letter-list-wrapper">
          <li class="letter-list" v-for="item of letterList" :key="item.id">{{item.letterName}}</li>
        </ul>
      </div>
      <div class="area all-city" v-for="item of allCityList" :key="item.id">
        <div class="area-title">
          {{item.title}}
        </div>
        <ul class="all-city-list-wrapper">
          <li class="all-list" v-for="list of item.cityList" :key="list.id">{{list.cityName}}</li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'CityList',
  props: {
    popularCity: String,
    letterSort: String,
    popularCityList: Array,
    outerPopularCityList: Array,
    letterList: Array,
    allCityList: Array,
    selected: Boolean
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .area-title
    text-indent $titleIndent
    height .8rem
    line-height .8rem
    font-size .2rem
    background #F5F5F5
  .popular-list-wrapper
    position relative
    overflow hidden
    &:before
      content: ''
      position absolute
      left 33.3%
      width 33.3%
      height 100%
      border-left .02rem solid #DDDDDD
      border-right .02rem solid #DDDDDD
    .popular-list
      width 33.3%
      float left
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
  .all-city-list-wrapper
    overflow hidden
    position relative
    .all-list
      width 25%;
      text-align center
      height .9rem
      line-height .9rem
      float left
      border-bottom .02rem solid #DDDDDD
      margin-bottom -1px
      ellipsis()
    &:before
      content: ''
      position absolute
      left 25%
      width 25%
      height 100%
      border-left .02rem solid #DDDDDD
      border-right .02rem solid #DDDDDD
    &:after
      content: ''
      position absolute
      left 75%
      width 25%
      height 100%
      border-left .02rem solid #DDDDDD
</style>
