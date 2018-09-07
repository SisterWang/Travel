<template>
  <div>
    <home-header :city="city"></home-header>
    <home-swiper :list="swiperList"></home-swiper>
    <home-icons :iconList="iconsList"></home-icons>
    <home-recommend :recommendList="recommendList"></home-recommend>
    <home-weekend :weekendList="weekendList"></home-weekend>
  </div>
</template>

<script>
// @ is an alias to /src
import HomeHeader from '@/components/Header.vue'
import HomeSwiper from '@/components/Swiper.vue'
import HomeIcons from '@/components/icons.vue'
import HomeRecommend from '@/components/recommend.vue'
import HomeWeekend from '@/components/weekend.vue'
import axios from 'axios'

export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  data () {
    return {
      city: '',
      swiperList: [],
      iconsList: [],
      recommendList: [],
      weekendList: []
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('/mock/index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.swiperList = data.swiperList
        this.city = data.city
        this.iconsList = data.iconsList
        this.recommendList = data.recommendList
        this.weekendList = data.weekendList
      }
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>
