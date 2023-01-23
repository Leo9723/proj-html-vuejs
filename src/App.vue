<script>
import AppHeader from './components/AppHeader.vue'
import AppJumbotron from './components/AppJumbotron.vue'

export default {
  components: {
    AppHeader,
    AppJumbotron
  }
}
</script>
<template lang="">
  <div>
    <AppHeader></AppHeader>
    <AppJumbotron></AppJumbotron>
  </div>
</template>
<style lang="scss">
      @use './components/styles/general.scss' as *

</style>
