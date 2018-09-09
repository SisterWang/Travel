<template>
    <div>
      <city-header></city-header>
      <city-search></city-search>
      <city-list :cities="cities" :hot="hotCities"></city-list>
      <alphabet :cities="cities"></alphabet>
    </div>
</template>

<script>
import axios from 'axios'
import CityHeader from '@/components/CityHeader.vue'
import CitySearch from '@/components/CitySearch.vue'
import CityList from '@/components/CityList.vue'
import Alphabet from '@/components/Alphabet.vue'

export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch,
    CityList,
    Alphabet
  },
  data () {
    return {
      cities: {},
      hotCities: [],

    }
  },
  methods: {
    getCityInfo () {
      axios.get('/mock/city.json')
        .then(this.handleGetCityInfoSucc)
    },
    handleGetCityInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.cities = data.cities
        this.hotCities = data.hotCities
      }
    }
  },
  mounted () {
    this.getCityInfo()
  }
}
</script>
