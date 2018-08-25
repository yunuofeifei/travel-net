<template>
<div class="icons">
  <swiper>
  <swiper-slide v-for="(page,index) of pages" :key="index">
  <div class="icon"  v-for="item of page" :key="item.id">
    <div class='icon-img'>
      <img class="icon-img-content" :src="item.imgUrl">
    </div>
    <p class="icon-desc">{{item.desc}}</p>
  </div>
  </swiper-slide>
</swiper>
</div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [{
        id: '0001',
        imgUrl: 'https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=2835524515,3980932591&fm=27&gp=0.jpg',
        desc: '景点门票'
      }, {
        id: '0002',
        imgUrl: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=1068465475,257788198&fm=202&mola=new&crop=v1',
        desc: '滑雪季'
      }, {
        id: '0003',
        imgUrl: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=3942084052,3894543838&fm=202&mola=new&crop=v1',
        desc: '泡温泉'
      }, {
        id: '0004',
        imgUrl: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=1409037549,3978854282&fm=202&mola=new&crop=v1',
        desc: '动物植物园'
      }, {
        id: '0005',
        imgUrl: 'https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=2835524515,3980932591&fm=27&gp=0.jpg',
        desc: '景点门票'
      }, {
        id: '0006',
        imgUrl: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=1068465475,257788198&fm=202&mola=new&crop=v1',
        desc: '滑雪季'
      }, {
        id: '0007',
        imgUrl: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=3942084052,3894543838&fm=202&mola=new&crop=v1',
        desc: '泡温泉'
      }, {
        id: '0008',
        imgUrl: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=1409037549,3978854282&fm=202&mola=new&crop=v1',
        desc: '动物植物园'
      }, {
        id: '0009',
        imgUrl: 'https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=2835524515,3980932591&fm=27&gp=0.jpg',
        desc: '景点门票'
      }, {
        id: '0010',
        imgUrl: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=1068465475,257788198&fm=202&mola=new&crop=v1',
        desc: '滑雪季'
      }, {
        id: '0011',
        imgUrl: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=3942084052,3894543838&fm=202&mola=new&crop=v1',
        desc: '泡温泉'
      }, {
        id: '0012',
        imgUrl: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=1409037549,3978854282&fm=202&mola=new&crop=v1',
        desc: '动物植物园'
      }, {
        id: '0013',
        imgUrl: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=1409037549,3978854282&fm=202&mola=new&crop=v1',
        desc: '动物植物园'
      }, {
        id: '0014',
        imgUrl: 'https://ss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=2835524515,3980932591&fm=27&gp=0.jpg',
        desc: '景点门票'
      }, {
        id: '0015',
        imgUrl: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=1068465475,257788198&fm=202&mola=new&crop=v1',
        desc: '滑雪季'
      }, {
        id: '0016',
        imgUrl: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=3942084052,3894543838&fm=202&mola=new&crop=v1',
        desc: '泡温泉'
      }, {
        id: '0017',
        imgUrl: 'https://ss3.baidu.com/-rVXeDTa2gU2pMbgoY3K/it/u=1409037549,3978854282&fm=202&mola=new&crop=v1',
        desc: '动物植物园'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
@import '~styles/mixins.styl'
.icons>>>.swiper-container
  background: #eee
  height: 0
  padding-bottom: 50%
.icons
  margin-top: .1rem
.icon
  position: relative
  overflow: hidden
  float: left
  width: 25%
  height: 0
  padding-bottom: 25%
.icon-img
  position: absolute
  top: 0
  left: 0
  right: 0
  bottom: .44rem
  box-sizing: border-box
  padding: .1rem
.icon-desc
  position: absolute
  left: 0
  right: 0
  bottom: 0
  height: .44rem
  line-height: .44rem
  color: $darkTextColor
  text-align: center
  ellipsis()
 .icon-img-content
  height: 100%
  display: block
  margin: 0 auto
</style>
