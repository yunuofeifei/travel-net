<template>
  <div>
    <div class="banner" @click="handleBanerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_140x140_80f63803.jpg"/>
      <div class="banner-info">
        <div class="banner-title">北京天安门AAAAA</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe796;</span>
            39
        </div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  components: {
    CommonGallary
  },
  methods: {
    handleBanerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_140x140_80f63803.jpg', 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_140x140_80f63803.jpg']
    }
  }
}
</script>

<style scoped lang="stylus">
.banner
  position: relative
  overflow: hidden
  height: 0
  padding-bottom: 55%
  .banner-img
    width: 100%
  .banner-info
    display: flex
    position: absolute
    left: 0
    right: 0
    bottom: 0
    line-height: .6rem
    background-image: linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,.8))
    color: #fff
    .banner-title
      flex: 1
      font-size: .32rem
      padding: 0 .14rem
    .banner-number
      padding: 0 .4rem
      line-height: .32rem
      height: .32rem
      border-radius: .2rem
      font-size: .24rem
      margin: .14rem 0
      background: rgba(0,0,0,.8)
      .banner-icon
        font-size: .24rem
</style>
