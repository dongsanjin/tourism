<template>
  <div class="other-wrapper">
    <div class="title">
      看了该景点的人还看了
    </div>
    <div>
      <ul>
        <li class="other-list" v-for="(list, index) of otherlist" :key="index">
          <div class="img-box">
            <img class="img-tag" :src="list.imgUrl" alt="">
          </div>
          <div class="info-box">
            <div class="price">
              <span class="money">￥<strong class="money-num">{{list.moneyNum}}</strong></span>起
            </div>
            <div class="info-title">
              {{list.title}}<span class="level">{{list.level}}</span>
            </div>
            <div class="assess">
              <span class="iconfont star">&#xe600;&#xe600;&#xe600;&#xe600;&#xe600;</span>
              <span class="assess-num">{{list.assessNum}}条评论</span>
            </div>
            <div class="area">{{list.area}}</div>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Other',
  data () {
    return {
      otherlist: [
        {
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1412/3f/f4d858b40070a2232c1f2ffb74d5e2aa.water.jpg_228x168_a77fa3ab.jpg',
          title: '锦里沟',
          level: '(4A)',
          assessNum: 2620,
          area: '武汉·黄陂区',
          moneyNum: 55
        },
        {
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1805/f9/f9fa2c4b30dc9f5aa3.img.jpg_228x168_815be30f.jpg',
          title: '木兰天池',
          level: '(5A)',
          assessNum: 6290,
          area: '武汉·黄陂区',
          moneyNum: 48
        },
        {
          imgUrl: 'http://img1.qunarzz.com/sight/p0/201212/20/aef8ac7cbef2738d93835fbb.jpg_228x168_745d565e.jpg',
          title: '木兰清凉寨',
          level: '(4A)',
          assessNum: 916,
          area: '武汉·黄陂区',
          moneyNum: 32
        },
        {
          imgUrl: 'http://img1.qunarzz.com/wugc/p35/201207/25/12403d5b2a3b747e93835fbb.jpg_228x168_2dee6672.jpg',
          title: '木兰山',
          level: '(4A)',
          assessNum: 388,
          area: '武汉·黄陂区',
          moneyNum: 53.5
        },
        {
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1501/f8/f8413365ed3e77ab.water.jpg_228x168_8707598b.jpg',
          title: '木兰草原',
          level: '(5A)',
          assessNum: 6287,
          area: '武汉·黄陂区',
          moneyNum: 64.5
        },
        {
          imgUrl: 'http://img1.qunarzz.com/sight/p0/1506/8b/9c2d25a9ea774f7ab6480eed523eeca8.water.jpg_228x168_f4460b69.jpg',
          title: '武汉姚家山旅游风景区',
          level: '',
          assessNum: 67,
          area: '武汉·黄陂区',
          moneyNum: 57
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
.other-wrapper
  margin-top .2rem
  background-color #fff
  .title
    position relative
    height .88rem
    line-height .88rem
    font-size .3rem
    padding-left .4rem
    &:before
      content: ''
      display block
      position absolute
      top 50%
      left .1rem
      width .06rem
      height .3rem
      transform translateY(-50%)
      background-color #1ba9ba
    &:after
      content: ''
      display block
      position absolute
      bottom 0
      left 0
      width 100%
      height 1px
      border-top 1px solid #dadada
      transform scaleY(.33333)
  .other-list
    position relative
    overflow hidden
    display flex
    padding .2rem 0 .2rem .2rem
    .img-box
      width 1.62rem
      height 1.62rem
      float left
      .img-tag
        width 100%
        height 100%
    .info-box
      position relative
      float left
      flex 1
      margin-left .2rem
      padding-right .2rem
      .price
        float right
        font-size .2rem
        .money
          color #ff9800
          .money-num
            font-size .36rem
            font-weight 400
      .info-title
        font-size .3rem
        .level
          color #adadad
      .assess
        margin-top .3rem
        font-size .2rem
        color #adadad
        .star
          color #ffb436
          font-size .2rem
        .assess-num
          margin-left .2rem
      .area
        margin-top .4rem
        font-size .2rem
        color #adadad
        text-indent .1rem
      &:after
        content: ''
        display block
        width 100%
        height 1px
        background-color #adadad
        transform scaleY(.33333)
        position absolute
        bottom -.2rem
        left 0
</style>
