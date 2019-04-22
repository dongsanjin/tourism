<template>
  <div class="wrapper">
    <section class="select-ticket">
      <div class="door select-active">
        门票
      </div>
      <div class="one">
        一日游
      </div>
      <div class="active"></div>
    </section>
    <section class="ticket">
      <ul>
        <li class="">
          <div class="ticket-type">

          </div>
          
        </li>
      </ul>
    </section>
  </div>
</template>
<script>
export default {
  name: 'Tecket'
}
</script>
<style lang="stylus" scoped>
  .wrapper
    margin-top .1rem
    background-color #fff
    height 5rem
    .select-ticket
      display flex
      position relative
      .door,
      .one
        flex 1
        text-align center
        font-size .3rem
        padding .2rem
      .active
        position absolute
        left 25%
        bottom 0
        width 1.4rem
        height .04rem
        transform translateX(-50%)
        background-color #00bcd4
      &:after
        content: ''
        display block
        height 1px
        width 100%
        position absolute
        left 0
        bottom 0
        background-color #e0e0e0
        transform scaleY(.33333)
</style>
