<template>
<div>
  <div class="title">周末去哪儿</div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
      <div class="item-img-wrapper">
        <img class="item-img" :src="item.imgUrl"/>
      </div>
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
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
      recommendList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/p/tts3/201408/09/8fc8e0f20aa09868c8d65eac.jpg_r_390x260x90_cc544545.jpg',
        title: '元气少女缘结神故居',
        desc: '元气满满的动漫世界，带你遨游'
      }, {
        id: '0002',
        imgUrl: 'https://imgs.qunarzz.com/p/tts4/1712/4c/fdfc6345e5220c02.jpg_r_390x260x90_9a27e83e.jpg',
        title: '元气少女缘结神故居',
        desc: '元气满满的动漫世界，带你遨游'
      }, {
        id: '0003',
        imgUrl: 'https://imgs.qunarzz.com/p/tts8/1703/94/61eb7ce216efc702.jpg_r_390x260x90_d5dd6341.jpg',
        title: '元气少女缘结神故居',
        desc: '元气满满的动漫世界，带你遨游'
      }, {
        id: '0004',
        imgUrl: 'https://imgs.qunarzz.com/p/tts1/1801/59/31bb5f1159fe9f02.jpg_r_390x260x90_a24e3d46.jpg',
        title: '元气少女缘结神故居',
        desc: '元气满满的动漫世界，带你遨游'
      }]
    }
  }
}
</script>

<style scoped lang="stylus">
@import '~styles/mixins.styl'
.title
  line-height: .8rem
  background: #eee
  text-indent: .2rem
  margin-top: .2rem
.item-img-wrapper
  height: 0
  overflow: hidden
  padding-bottom: 35%
.item-img
  width: 100%
.item-info
  padding: .1rem
.item-title
  line-height: .54rem
  font-size: .32rem
  ellipsis()
.item-desc
  line-height: .4rem
  ellipsis()
  color: #ccc
</style>
