<template>
  <div id="HOME">
    <HeaderComponent />
    <MainComponent/>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import MainComponent from './components/MainComponent.vue'
export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent
  }
}
</script>

<style lang="scss">
button{
  text-transform: uppercase!important;
  border-radius: 0!important;
  padding-left: 20px!important;
  padding-right: 20px!important;
}
</style>
