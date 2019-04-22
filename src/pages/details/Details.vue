<template>
  <div class="wrapper">
    <banner></banner>
    <details-header></details-header>
    <details-attractions></details-attractions>
    <details-recommend></details-recommend>
    <details-assess></details-assess>
    <details-other></details-other>
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
export default {
  name: 'Details',
  data () {
    return {
      showDesc: false
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
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper
      background-color #f5f5f5
</style>
