<template>
  <div>
    <city-header></city-header>
    <city-territory></city-territory>
    <city-list></city-list>
  </div>
</template>
<script>
import CityHeader from './components/Header'
import CityTerritory from './components/Territory'
import CityList from './components/List'
export default {
  name: 'City',
  components: {
    CityHeader,
    CityTerritory,
    CityList
  }
}
</script>
<style lang="stylus" scoped>
</style>
