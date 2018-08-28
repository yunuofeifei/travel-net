<template>
  <div>
    <div class="banner" @click="handleBanerClick">
      <img class="banner-img" :src="bannerImg"/>
      <div class="banner-info">
        <div class="banner-title">{{this.sightName}}</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe796;</span>
            {{this.gallaryImgs.length}}
        </div>
      </div>
    </div>
    <common-gallary
      :imgs="gallaryImgs"
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
  props: {
    sightName: String,
    bannerImg: String,
    gallaryImgs: Array
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
      showGallary: false
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
