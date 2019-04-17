<template>
  <div class="clear">
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="attractions" v-for="(item, index) of attractionsList" :key="index">
        <div class="attractions-img-wrapper">
          <img :src="item.imgUrl" class="attractions-img">
        </div>
        <div class="attractions-info">
          <p class="attractions-title">{{item.title}}</p>
          <p class="attractions-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      attractionsList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/d5/abe8a48a6ef8bf.jpg_r_640x214_7c41cc81.jpg',
        title: '武汉必打卡',
        desc: '到武汉感受神奇的热干面之都'
      },
      {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/6d/5afbf529076ef6.jpg_r_640x214_7414b151.jpg',
        title: '三峡人家',
        desc: '感受长江的水三峡的情怀，自古至今，无数骚人墨客浓墨重彩的描绘三峡，赶紧领略三峡的壮美吧！'
      },
      {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/fe/2533da6335a59d.jpg_r_640x214_9fb62f4b.jpg',
        title: '武汉踏青赏花胜地',
        desc: '人间四月芳菲尽，武汉踏青赏花正当时'
      },
      {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/4f/95a94c90ef3521.jpg_r_640x214_345412f9.jpg',
        title: '开启亲子时光',
        desc: '远离喧嚣的都市，带孩子去一个幽静，清新的天然“氧吧”，呼吸新鲜空气，亲近自然健康成长'
      },
      {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1507/e0/4aae49007c8a64.jpg_r_640x214_65a42783.jpg',
        title: '周末出游乐翻天',
        desc: '周末，想去哪儿就去哪儿~'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .clear::after
    content: ''
    display block
    height 0
    clear both
  .title
    height .8rem
    line-height .8rem
    text-indent $titleIndent
    background-color #F5F5F5
  .attractions-img-wrapper
    overflow hidden
    height 0
    padding-bottom 37%
    .attractions-img
      width 100%
  .attractions-info
    height 1rem
    padding .1rem 0
    .attractions-title
      height .6rem
      line-height .6rem
      text-indent $descIndent
    .attractions-desc
      text-indent $descIndent
      font-size .24rem
      color #737373
      width 82%
      ellipsis()
</style>
