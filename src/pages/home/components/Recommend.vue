<template>
<div>
  <div class="title">热销推荐</div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
      <img class="item-img" :src="item.imgUrl"/>
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
        <button class="item-button">查看详情</button>
      </div>
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name: 'Recommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=3731123091,1350898344&fm=27&gp=0.jpg',
        title: '元气少女缘结神故居',
        desc: '元气满满的动漫世界，带你遨游'
      }, {
        id: '0002',
        imgUrl: 'https://ss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=225089870,1031568935&fm=27&gp=0.jpg',
        title: '元气少女缘结神故居',
        desc: '元气满满的动漫世界，带你遨游'
      }, {
        id: '0003',
        imgUrl: 'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=479278155,1957704465&fm=27&gp=0.jpg',
        title: '元气少女缘结神故居',
        desc: '元气满满的动漫世界，带你遨游'
      }, {
        id: '0004',
        imgUrl: 'https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=1242153218,2154315500&fm=27&gp=0.jpg',
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
 .item
  overflow: hidden
  display: flex
  height: 1.9rem
.item-img
  width: 1.7rem
  height: 1.7rem
  padding: .1rem
.item-info
  flex: 1
  padding: .1rem
  min-width: 0
.item-title
  line-height: .54rem
  font-size: .32rem
  ellipsis()
.item-desc
  line-height: .4rem
  ellipsis()
  color: #ccc
.item-button
  background: #ff9300
  padding: 0 .2rem
  border-radius: .06rem
  color: #fff
  margin-top: .02rem
  line-height: .44rem
  height: .44rem
</style>
