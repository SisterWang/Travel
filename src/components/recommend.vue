<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
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
  name: 'HomeRecommend',
  data: function () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1701/c0/c0899de1bcef6f9a3.img.jpg_200x200_b5b00164.jpg',
        title: '南昌新中原大剧院',
        desc: '好看的剧院'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1610/16/165075d3fcbe7c8ba3.water.jpg_200x200_dacfbf65.jpg',
        title: '南昌万达海洋乐园',
        desc: '浪漫南昌首站，浪漫的海洋主题乐园'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201310/08/8a668cb269731796c8d65eac.png_200x200_4af34935.png',
        title: '南昌琴岛之夜',
        desc: '浪漫爱琴岛'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .title
    line-height: .8rem
    background: #eee
    text-indent: .2rem
    margin-top: .2rem
  .item
    display: flex
    height: 1.9rem
    overflow: hidden
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
        overflow: hidden
        white-space: nowrap
        text-overflow: ellipsis
      .item-desc
        line-height: .4rem
        color: #ccc
        overflow: hidden
        white-space: nowrap
        text-overflow: ellipsis
      .item-button
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        margin-top: .2rem
        color: #fff
        line-height: .44rem
</style>
