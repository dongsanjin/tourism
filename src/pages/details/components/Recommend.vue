<template>
  <div class="recomment-wrapper">
    <section class="title">
      <h3>去哪儿推荐</h3>
    </section>
    <section class="recomment-location">
      <ul>
        <li class="location-list" v-for="(list, index) of locationList" :key="index">
          <div class="list-left">
            <p class="list-title">{{list.title}}</p>
            <div class="list-time">
              <img class="img-tag" src="https://img1.qunarzz.com/piao/fusion/1804/25/792e9929973a9902.png">
              23:59前可订明日
            </div>
            <div class="list-label">
              <div class="list-nature list-box" v-if="list.self">
                <img class="list-img-tag" src="https://img1.qunarzz.com/piao/fusion/1804/b0/c3cf2897c74ecc02.png">
                自营
              </div>
              <div class="label-time list-box" v-if="list.retreat">
                随时退
              </div>
            </div>
          </div>
          <div class="list-right">
            <p class="money">￥<span class="money-number">{{list.moneyNum}}</span></p>
            <div class="booking">预订</div>
          </div>
        </li>
      </ul>
    </section>
  </div>
</template>
<script>
export default {
  name: 'Recommend',
  data () {
    return {
      locationList: [
        {
          title: 'Q木兰云雾山门票成人票',
          self: true,
          retreat: true,
          moneyNum: 60
        },
        {
          title: '【高尚】云雾山成人票',
          self: false,
          retreat: true,
          moneyNum: 58
        },
        {
          title: '木兰云雾山学生/儿童/老人票',
          self: false,
          retreat: true,
          moneyNum: 35
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .recomment-wrapper
    margin-top 2rem
    width 100%
    background-color #fff
    .title
      position relative
      height .86rem
      line-height .86rem
      text-indent .8rem
      font-size .32rem
      background .2rem center no-repeat url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAwCAMAAABg3Am1AAAAflBMVEUAAAD/bm7/b2//b2//eXn/b2//b2//bm7/b2//b2//bm7/b2//b2//b2//bm7/b2//b2//cXH/eHj/qqr/bm7/////cXH/iIj/oqL//f3/mJj/fHz/9/f/8PD/4eH/ycn/6+v/1dX/0ND/t7f/ra3/kpL/jo7/c3P/5ub/vr7o37bEAAAAFHRSTlMA9uZeCfny7NvLt6+PfGZONxsRA/pz1k8AAAFrSURBVEjHpZbZdoMwDERtMEvYE8YJZN/b/v8PNvicJsiYqJzcB548WGNZksUAVWZJHAVBFCdZqQTDwk8lesjUX4hxVB5iQJiPbVMXHpx4RS0czGcYZTYXAyoPb/AqYeFLvEX61nqwEEUlwSKrnl9X/JtmZfl4Oq9d53Pfan2yzurvdAs42OsHaxAKYVDOA207wcEKShlBDhfaIUBu7lsIl2UjuIASLkZTsDaCxpWMFC7ORrCBRfqw7MxZY9Z/w0YqUWLI8tLqJ+25n8BSZP3Am+aG2/Vw1IQ9XmQiwZNV9z+0mkKtJCKmAg094IgXsYg4Ab0gkQh4wRUvgv8I1kTAh7QHCYk3fQIxnbCCHXokImMFPyCJKznB9gvkaijJ7XCnl0+kU3ZISQFttp3DnWW5oQVES3S57D4Eq0RJE+DJSZvh8RRpZDwFaZU8s5o0YxZvPrXdTx0on40sfih+Nnb5wT7x6fDR42Ty8+cXnHyOvDgQEbUAAAAASUVORK5CYII=')
      background-size 5%
    .location-list
      overflow hidden
      position relative
      padding .3rem .2rem
      &:before
        position absolute
        left 2%
        top 0
        content: ''
        width 96%
        height 1px
        transform scaleY(.33333)
        background-color #e0e0e0
      .list-left
        float left
        .list-title
          font-size .32rem
        .list-time
          height .24rem
          line-height .24rem
          font-size .2rem
          margin .06rem 0 .16rem
          color #616161
          .img-tag
            height 100%
            vertical-align baseline
        .list-label
          .list-box
            height .3rem
            line-height .3rem
            font-size .24rem
            display inline-block
            border 1px solid #a5e4ec
            border-radius .08rem
            text-align center
            color #00afc7
            padding 0 .02rem
            .list-img-tag
              height 50%
      .list-right
        float right
        text-align center
        .money
          color #ff9800
          font-size .24rem
          .money-number
            font-size .4rem
        .booking
          width 1.8rem
          height .6rem
          line-height .6rem
          font-size .28rem
          color #ffffff
          border-radius .06rem
          background-color #ff9800
</style>
