<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1701/c0/c0899de1bcef6f9a3.img.jpg_600x330_b93f75a5.jpg">
      <div class="banner-info">
        <div class="banner-number">
          <span class="iconfont">&#xe796;</span>
          1
        </div>
        <div class="banner-title">
          南昌新中原大剧院
        </div>
      </div>
    </div>
    <gallary
    :imgs="imgs"
    v-show="showGallary"
    @close="handleGallaryClose"
    ></gallary>
  </div>
</template>

<script>
import Gallary from '@/components/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/1701/c0/c0899de1bcef6f9a3.img.jpg_r_800x800_2a7663a4.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    Gallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      displau: flex
      position: absolute
      left: 0
      right: 0
      bottom: .2rem
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(to top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex: 1
        font-size: .36rem
        padding: 0 .2rem
      .banner-number
        margin: 0 .3rem
        height: .3rem
        width: 1.2rem
        line-height: .3rem
        border-radius: .2rem
        background: rgba(0, 0, 0, .8)
        text-align: center
</style>
