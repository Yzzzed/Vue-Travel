<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1507/f0/45ad118808cbfbdd1ca292f6939bdda5.water.jpg_600x330_0ac4cfae.jpg">
      <div class="banner-info">
        <div class="banner-title">大连圣亚海洋世界</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe617;</span>39</div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  components: {
    CommonGallary
  },
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1507/f0/45ad118808cbfbdd1ca292f6939bdda5.water.jpg_r_800x800_7fe83f3e.jpg', 'http://img1.qunarzz.com/sight/p0/1709/35/35181b88573d6be5a3.img.png_r_800x800_7ea3cc9a.png']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      display flex
      position absolute
      left 0
      right 0
      bottom 0
      line-height .6rem
      color #fff
      background-image linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, .8))
      .banner-title
        flex 1
        padding 0 .2rem
        font-size .32rem
      .banner-number
        margin-top .14rem
        padding 0 .4rem
        height .32rem
        line-height .32rem
        border-radius .2rem
        background rgba(0, 0, 0, .8)
        font-size .24rem
        .banner-icon
          padding 0 0.1rem
          font-size .24rem
</style>
