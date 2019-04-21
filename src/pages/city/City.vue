<template>
  <div>
    <city-header :selectCity="selectCity"></city-header>
    <city-territory @sendSelectedValue="changeSelectedValue" :selected="selected"></city-territory>
    <city-list :popularCity="popularCity" :letterSort="letterSort" :popularCityList="popularCityList"
    :letterList="letterList" :allCityList="allCityList" :outerPopularCityList="outerPopularCityList" :selected="selected" :allOverseasCityList="allOverseasCityList" :overseasLetterList="overseasLetterList"></city-list>
  </div>
</template>
<script>
import CityHeader from './components/Header'
import CityTerritory from './components/Territory'
import CityList from './components/List'
import axios from 'axios'
export default {
  name: 'City',
  components: {
    CityHeader,
    CityTerritory,
    CityList
  },
  data () {
    return {
      selected: true,
      selectCity: '',
      popularCity: '',
      letterSort: '',
      popularCityList: [],
      outerPopularCityList: [],
      letterList: [],
      allCityList: [],
      allOverseasCityList: [],
      overseasLetterList: []
    }
  },
  methods: {
    getHomeInfo () {
      axios.get('/api/city.json')
        .then(this.getCityInfoSucc)
    },
    getCityInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.selectCity = data.selectCity
        this.popularCity = data.popularCity
        this.letterSort = data.letterSort
        this.popularCityList = data.popularCityList
        this.letterList = data.letterList
        this.allCityList = data.allCityList
        this.outerPopularCityList = data.outerPopularCityList
        this.allOverseasCityList = data.allOverseasCityList
        this.overseasLetterList = data.overseasLetterList
      }
    },
    changeSelectedValue (val) {
      this.selected = val
    }
  },
  mounted () {
    this.getHomeInfo()
  }
}
</script>
<style lang="stylus" scoped>
</style>
