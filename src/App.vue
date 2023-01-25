<script>
import AppHeader from './components/AppHeader.vue'
import AppSecondaryHeader from './components/AppSecondaryHeader.vue'
import AppJumbotron from './components/AppJumbotron.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  components: {
    AppHeader,
    AppSecondaryHeader,
    AppJumbotron,
    AppMain,
    AppFooter
  },
  data(){
    return{
      hover: false
    }
  },
  methods:{
    headerShow(){
            this.hover = true
        },
        headerHide(){
            this.hover = false
        }
  }
}
</script>
<template lang="">
  <div>
    <AppHeader :class="(hover) ? 'h-0' :'h-100'"></AppHeader>
    <AppSecondaryHeader :class="(hover) ? 'h-100' : 'h-0'"></AppSecondaryHeader>
    <div class="primary-header" @mouseover="headerHide">
      <AppJumbotron></AppJumbotron>
    </div>
    <div class="secondary-header" @mouseover="headerShow">
      <AppMain></AppMain>
      <AppFooter></AppFooter>
    </div>
  </div>
</template>
<style lang="scss">
      @use './components/styles/general.scss' as *;

  .secondary-header-cont{
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
    z-index: 5;
    box-shadow: 0px 0px 30px 5px rgba(114, 114, 114, 0.384);
    transition: all 0.5s;
  }
  .h-0{
    height: 0px;
    opacity: 0;
  }
  .h-100{
    height: 50px;
    opacity: 1;
  }
</style>
