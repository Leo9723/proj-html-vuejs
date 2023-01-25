<script>
/* elementi principali */
import AppHeader from './components/AppHeader.vue'
import AppSecondaryHeader from './components/AppSecondaryHeader.vue'
import AppJumbotron from './components/AppJumbotron.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
/* elementi in fixed */
import AppBack from './components/AppBack.vue'
import AppNav from './components/AppNav.vue'
import AppChat from './components/AppChat.vue'

export default {
  components: {
    AppHeader,
    AppSecondaryHeader,
    AppJumbotron,
    AppMain,
    AppFooter,
    AppBack,
    AppNav,
    AppChat
  },
  data(){
    return{
      /* valore cangiante per l'apparizione della barra header secondaria */
      hover: false,
      /* valore cangiante per l'apparizione nel footer del tasto per tornare ad inizio pagina */
      backScroll : false
    }
  },
  methods:{
    /* cambio valori header */
    headerShow(){
            this.hover = true
        },
    headerHide(){
        this.hover = false
    },
    /* cambio valori backButton */
    backShow(){
      this.backScroll = true
    },
    backHide(){
      this.backScroll = false
    }

  }
}
</script>
<template lang="">
  <div>
    <!-- imposto classi invertite a seconda del valore per intercambiare i due header -->
    <AppHeader :class="(hover) ? 'h-0' :'h-100'"></AppHeader>
    <AppSecondaryHeader :class="(hover) ? 'h-100' : 'h-0'"></AppSecondaryHeader>
    <AppNav></AppNav>
    <!-- triggero l'evento che intercambia i due header -->
      <AppJumbotron @mouseover="headerHide"></AppJumbotron>
      <AppMain @mouseover="headerShow"></AppMain>
      <!-- imposto la classe che mi mostrerà il backButton solo se mi trovo nel footer -->
        <AppBack :class="(backScroll) ? 'show-back' : 'hide-back'" @mouseover="backShow" @mouseout="backHide"></AppBack>
        <AppChat @mouseover="backShow" @mouseout="backHide"></AppChat>
        <AppFooter @mouseover="backShow" @mouseout="backHide"></AppFooter>
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
  .back-button{
    position: fixed;
    top: 80%;
    left: 95%;
    transition: all 0.5s;
  }
  .chat-button{
    position: fixed;
    top: 90%;
    left: 95%;
    transition: all 0.5s;
  }
  .show-back{
    opacity: 1;
  }
  .hide-back{
    opacity: 0;
  }
</style>
