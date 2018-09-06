<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl">
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
  data: function () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/74/a665dfecf12ae.jpg_r_640x214_5d22909a.jpg',
        title: '南昌必游top10',
        desc: '看山看水，看看历史对南昌的浸润'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/df/9bcc134d126bc4.jpg_r_640x214_58a1f389.jpg',
        title: '陶醉青山绿水间',
        desc: '整个城市青山环绕，湖泊点缀其间'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/bd/688c12889af7ad.jpg_r_640x214_cc490c32.jpg',
        title: '带着宝贝玩乐',
        desc: '全家出游，可以说是再好不过的美事了'
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
  .item-img-wrapper
    height: 0
    overflow: hidden
    padding-bottom: 33.9%
    .item-img
      width: 100%
  .item-info
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
</style>
