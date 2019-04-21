<template>
  <div>
    <details-header></details-header>
    <details-list></details-list>
  </div>
</template>
<script>
import DetailsHeader from './album/Header'
import DetailsList from './album/List'
export default {
  name: 'Album',
  components: {
    DetailsHeader,
    DetailsList
  }
}
</script>
<style lang="stylus" scoped>
</style>
