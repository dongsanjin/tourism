<template>
  <div class="wrapper">
    <div class="title">
      用户评价
    </div>
    <section class="assess">
      <ul>
        <li class="assess-wrapeer" v-for="user of userList" :key="user.id">
          <div class="assess-header">
            <span class="assess-star iconfont"><span class="good">&#xe600;&#xe600;&#xe600;&#xe600;&#xe600;</span></span>
            <span class="assess-user">{{user.name + ' ' + user.time}}</span>
          </div>
          <p class="assess-desc" :ref="user.id">{{user.desc}}</p>
          <div class="expand iconfont iconicon"></div>
          <div class="imgs-wrapper">
            <ul>
              <li class="img-list" v-for="(list, index) of user.imgsList" :key="index">
                <img class="img-tag" :src="list.imgUrl">
              </li>
            </ul>
          </div>
        </li>
      </ul>
    </section>
    <section class="all-assess">
      查看全部评论<span class="iconfont">&#xe643;</span>
    </section>
  </div>
</template>
<script>
export default {
  name: 'Assess',
  data () {
    return {
      userList: [
        {
          name: '勇*豆',
          time: '2019-03-30',
          desc: '杜娟花半开半盛，很夺目！美得想尖叫！四月去就是全盛期！有五六个停车场，要早点去，不塞车，而且可以停在里面的停车场，走路的路程短一点。三个景点的观光车，门口到竹林寺到花海到花宇山，每段十元，可以选择先上花宇山，再分段下来，也可以先分段，再从花宇山下来，不要想着走路上去，除非你时间充足又有超人的体力！竹林寺慎入！进去可以免费烧香，磕头后，和尚会监督你投香火钱，投了钱立刻走，不要接受他们的红丝带，拿了红丝带就得听他讲解，可能还要点香油灯，那就没完没了啦！没小孩的直接这三个景点去就足够了，有小孩的可以去恐龙园冰雕馆玩玩。景区内只有小卖部，最好自带干粮。',
          imgsList: [
            {
              imgUrl: 'http://mp-commentcp.qunarzz.com/mp_comment_mp_comment/1554232254200100912000000tdp2y2BA8_D_640_10000.jpg_228x168_66a1f951.jpg'
            },
            {
              imgUrl: 'http://mp-commentcp.qunarzz.com/mp_comment_mp_comment/1554232254314100912000000tdp2z3B45_D_640_10000.jpg_228x168_8ac8d2b9.jpg'
            },
            {
              imgUrl: 'http://mp-commentcp.qunarzz.com/mp_comment_mp_comment/1554232254503100u12000000tb9k8D577_D_640_10000.jpg_228x168_a7e0951b.jpg'
            },
            {
              imgUrl: 'http://mp-commentcp.qunarzz.com/mp_comment_mp_comment/1554232254826100v12000000tmc9z2E1A_D_640_10000.jpg_228x168_0c9d4ac5.jpg'
            },
            {
              imgUrl: 'http://mp-commentcp.qunarzz.com/mp_comment_mp_comment/1554232255118100p12000000tafbqF124_D_640_10000.jpg_228x168_4dde43d1.jpg'
            },
            {
              imgUrl: 'http://mp-commentcp.qunarzz.com/mp_comment_mp_comment/1554232255474100112000000to7ud65C9_D_640_10000.jpg_228x168_c89973b6.jpg'
            }
          ]
        },
        {
          name: 'J*r',
          time: '2018-04-16',
          desc: '2018年4月15日去，正是花开茂盛时，满山遍野杜鹃花，景色非常美，感觉不是一两张照片可以形容的。但是景区管理非常混乱，体验好感为0，这个5A景区给它1A还怕它骄傲，自驾过去两个小时，从景区大门就开始徒步上山到下山步行一共6个小时。景区内有观光车，一共三段路每段路收费10元，每段路有固定的售票点，人上山的路就是盘山公路，和观光车是并行的，路上人很多，所有的观光车从身边路过都会按喇叭，整个景区都是车的喇叭声和扬起的灰尘和尾气。走了差不多两个小时就到了花海花洋的山脚下，此时真正的赏花才开始，路都是在花丛中建的，很陡，但惊艳的景色不停的映入眼帘，美不胜收。一波波大簇大簇的杜鹃颜色各异，有粉红的，有大红的，走几步都会停下拍几张。总之赏花这段非常满意，让我们大饱眼福。好了，到了下山的时候了，第一个售票点人太多因为大家都是刚赏完花回来，我们决定走到下一段路买票下山，走了差不多30分钟到了，结果人家窗口关闭了说票已卖完，自己走下山……当是才3点多票就卖完了，此时腿已废也没办法。最后，整个游玩给大家的建议：1，门票60，停车费10，还是直接在门口买个全程的观光车票30，下山也买个全程下山的车票30，因为从景区门口到花海脚下没什么景点，都是盘山公路。2，花海赏花建议从一边上另一边下，很多人都是从上去的路下来造成拥堵，从另一边下的时候发现走的人很少景色更美。',
          imgsList: [
            {
              imgUrl: 'http://img1.qunarzz.com/p/tts1/1804/28/ed7840f1136dee02.jpg_228x168_2d8ade77.jpg'
            },
            {
              imgUrl: 'http://img1.qunarzz.com/p/tts1/1804/e9/ae693b8d1b2dc302.jpg_228x168_29152a8c.jpg'
            },
            {
              imgUrl: 'http://img1.qunarzz.com/p/tts2/1804/5b/685cbf4502867402.jpg_228x168_daac5fc8.jpg'
            },
            {
              imgUrl: 'http://img1.qunarzz.com/p/tts4/1804/84/56a1ad624e41e602.jpg_228x168_90d9f3e7.jpg'
            },
            {
              imgUrl: 'http://img1.qunarzz.com/p/tts1/1804/b9/6524236151de2f02.jpg_228x168_f6e6aec0.jpg'
            },
            {
              imgUrl: 'http://img1.qunarzz.com/p/tts6/1804/11/abe5da266217e602.jpg_228x168_e141ed94.jpg'
            }
          ]
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper
    overflow hidden
    margin-top .1rem
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
    .assess-wrapeer
      position relative
      padding .2rem
      margin-bottom .2rem
      &:before
        content: ''
        display block
        position absolute
        top 0
        left 0
        height 1px
        width 100%
        border-bottom 1px solid #e0e0e0
        transform scaleY(.33333)
      .assess-header
        overflow hidden
        padding-top .1rem
        font-size .2rem
        .assess-star
          float left
          font-size .26rem
          .good
            color orange
        .assess-user
          float right
      .assess-desc
        overflow hidden
        margin-top .2rem
        font-size .26rem
        color #616161
        height 2rem
        line-height .4rem
      .expand
        text-align center
        font-size .4rem
        margin-bottom .2rem
      .imgs-wrapper
        overflow hidden
        .img-list
          float left
          width 33%
          margin-bottom .1rem
          padding 0 .05rem
          box-sizing border-box
          .img-tag
            width 100%
    .all-assess
      position relative
      height .8rem
      line-height .8rem
      text-align center
      &:before
        content: ''
        display block
        position absolute
        top 0
        left 0
        height 1px
        width 100%
        border-top 1px dashed #dadada
        transform scaleY(.33333)
</style>
