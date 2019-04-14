<template>
  <div>

    <!-- 根据selected的值来显示境内内容还是境外内容  默认为true显示境内内容 -->
    <div v-if="selected">

      <!-- 境内热门城市 -->
      <div class="area popular-city">
        <div class="area-title">
          {{popularCity}}
        </div>
        <ul class="popular-list-wrapper">
          <li class="popular-list" v-for="item of popularCityList" :key="item.id" @click="handleCityClick(item.listName)">{{item.listName}}</li>
        </ul>
      </div>

      <!-- 字母排序部分 -->
      <div class="area area-letter">
        <div class="area-title">
          {{letterSort}}
        </div>
        <ul class="letter-list-wrapper wrapper">
          <li class="letter-list" v-for="item of letterList" :key="item.id" @click="goArea">{{item.letterName}}</li>
        </ul>
      </div>

      <!-- 通过字母来区分的所有境内城市 -->
      <div class="area all-city" v-for="item of allCityList" :key="item.id"  :ref="item.title" :id="item.title">
        <div class="area-title">
          {{item.title}}
        </div>
        <ul class="all-city-list-wrapper">
          <li class="all-list" v-for="list of item.cityList" :key="list.id"
          @click="handleCityClick(list.cityName)">{{list.cityName}}</li>
        </ul>
      </div>
    </div>

    <!-- 当selected为false时 -->
    <div v-else>
      <!-- 热门城市部分 -->
      <div class="area popular-city">
        <div class="area-title">
          {{popularCity}}
        </div>
        <ul class="popular-list-wrapper">
          <li class="popular-list" v-for="item of outerPopularCityList" :key="item.id">{{item.listName}}</li>
        </ul>
      </div>

      <!-- 字母排序部分 -->
      <div class="area area-letter">
        <div class="area-title">
          {{letterSort}}
        </div>
        <ul class="letter-list-wrapper">
          <li class="letter-list" v-for="item of letterList" :key="item.id">{{item.letterName}}</li>
        </ul>
      </div>

      <!-- 通过字母来区分的所有境外城市 -->
      <div class="area all-city" v-for="item of allCityList" :key="item.id" :id="item.title">
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
import { mapMutations } from 'vuex'

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
  },
  data () {
    return {
      goTo: String
    }
  },
  methods: {
    goArea (el) {
      const elem = this.$refs[el.target.innerText][0]
      elem.scrollIntoView(true)
    },
    handleCityClick (cityName) {
      this.changeCity(cityName)
      this.$router.push('/')
    },
    ...mapMutations(['changeCity'])
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
      //设置负值的z-index，防止其覆盖的list元素不能触发点击事件
      z-index -1
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
      //设置负值的z-index，防止其覆盖的list元素不能触发点击事件
      z-index -1
    &:after
      content: ''
      position absolute
      left 75%
      width 25%
      height 100%
      border-left .02rem solid #DDDDDD
      //设置负值的z-index，防止其覆盖的list元素不能触发点击事件
      z-index -1
</style>
