<template>
  <div class="wrapper">
    <banner></banner>
    <details-header></details-header>
    <details-attractions></details-attractions>
    <details-recommend></details-recommend>
    <details-assess></details-assess>
    <details-other></details-other>
    <div class="h"></div>
  </div>
</template>
<script>
import Banner from './components/Banner'
import DetailsHeader from './components/Header'
import DetailsAttractions from './components/Attractions'
import DetailsRecommend from './components/Recommend'
import DetailsAssess from './components/Assess'
import DetailsOther from './components/Other'
export default {
  name: 'Details',
  components: {
    Banner,
    DetailsHeader,
    DetailsRecommend,
    DetailsAttractions,
    DetailsAssess,
    DetailsOther
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper
      background-color #f5f5f5
    .h
      height 20rem
</style>
