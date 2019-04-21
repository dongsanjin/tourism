<template>
  <div>
    <banner></banner>
    <details-header></details-header>
    <div class="h"></div>
  </div>
</template>
<script>
import Banner from './components/Banner'
import DetailsHeader from './components/Header'
export default {
  name: 'Details',
  components: {
    Banner,
    DetailsHeader
  }
}
</script>
<style lang="stylus" scoped>
  .h
    height 20rem
</style>
