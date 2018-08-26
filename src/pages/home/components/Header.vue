<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
    输入城市经典、游玩主题
   </div>
   <router-link to="/city">
      <div class="header-right">{{this.doubleCity}}
        <span class="iconfont arrow-icon">&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState, mapGetters } from 'vuex'
export default {
  name: 'Home',
  computed: {
    ...mapState(['city']),
    ...mapGetters(['doubleCity'])
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.header
  display: flex
  line-height: .86rem
  background: $bgColor
  color: #fff
.header-left
  width: .64rem
  float: left
.back-icon
   text-align: center;
   font-size: .4rem;
.header-input
  flex: 1
  background: #fff
  border-radius: .1rem
  margin-top: .12rem
  margin-left: .2rem
  height: .64rem
  color: #ccc
  line-height: .64rem
  padding-left: .2rem
.header-right
  min-width: 1.04rem
  padding: 0 .1rem
  float: right
  text-align: center
  color: #fff
.arrow-icon{
  margin-left: -.04rem;
  font-size: .24rem;
}
</style>
