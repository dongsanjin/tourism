<template>
  <div class="city-wrapper">
    <div class="city">
      <div class="city-inner city-active">
        境内
      </div>
      <div class="city-outer">
        境外·港澳台
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'CityTerritory'
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles'
.city-wrapper
  overflow hidden
  background-color $bgColor
  height 0
  padding-bottom 8%
  .city
    display flex
    width 75%
    border 1px solid #fff
    margin 0 auto
    border-radius .05rem
    .city-inner
    .city-outer
      flex 1
      text-align center
      padding .08rem
      color #fff
    .city-active
      background-color #fff
      color $bgColor
</style>
