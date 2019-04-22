<template>
  <div class="wrapper">
    <banner></banner>
    <details-header :headerTitle="headerTitle"></details-header>
    <details-attractions :attractionsObj="attractionsObj"></details-attractions>
    <details-recommend :locationList="locationList"></details-recommend>
    <details-assess :userList="userList"></details-assess>
    <details-other :otherlist="otherlist"></details-other>
    <details-footer></details-footer>
  </div>
</template>
<script>
import Banner from './components/Banner'
import DetailsHeader from './components/Header'
import DetailsAttractions from './components/Attractions'
import DetailsRecommend from './components/Recommend'
import DetailsAssess from './components/Assess'
import DetailsOther from './components/Other'
import DetailsFooter from './components/Footer'
import axios from 'axios'
export default {
  name: 'Details',
  data () {
    return {
      showDesc: false,
      headerTitle: '',
      attractionsObj: {},
      locationList: [],
      userList: [],
      otherlist: []
    }
  },
  components: {
    Banner,
    DetailsHeader,
    DetailsRecommend,
    DetailsAttractions,
    DetailsAssess,
    DetailsOther,
    DetailsFooter
  },
  methods: {
    getDetailsJson () {
      axios.get('/api/details.json')
        .then(this.getDetailsData)
    },
    getDetailsData (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.headerTitle = data.headerTitle
        this.attractionsObj = data.attractionsObj
        this.locationList = data.locationList
        this.userList = data.userList
        this.otherlist = data.otherlist
      }
      console.log(this.attractionsObj)
    }
  },
  mounted () {
    this.getDetailsJson()
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper
      background-color #f5f5f5
</style>
