<template>
  <div>
    <div class="city-wrapper">
      <div class="city">
        <div class="city-inner city-active" @click="addAraeClick" >
          境内
        </div>
        <div class="city-outer" @click="addAraeClick">
          境外·港澳台
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'CityTerritory',
  props: {
    selected: Boolean
  },
  data () {
    return {
      selectedclone: this.selected
    }
  },
  methods: {
    addAraeClick () {
      let btns = document.querySelector('.city').querySelectorAll('div')
      btns.forEach((el) => {
        el.addEventListener('click', () => {
          if (!el.classList.contains('city-active')) {
            this.selectedclone = !this.selectedclone
            for (let item of btns) {
              item.classList.toggle('city-active')
            }
            this.$emit('sendSelectedValue', this.selectedclone)
          }
        })
      })
    }
  },
  mounted () {
    this.addAraeClick()
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles'
@import '~styles/mixins.styl'
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
