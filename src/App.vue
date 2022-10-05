<template>
  <div id="HOME">
    <HeaderComponent />
    <MainComponent/>
    <FooterComponent/>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import MainComponent from './components/MainComponent.vue'
import FooterComponent from './components/FooterComponent.vue'
export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
    FooterComponent,
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
.line-warning{
  width: 180px;
  height: 5px;
  background-color: #fcd66c;
  }
  .font-20{
    font-size: 20px;
    color: #78787b;
  }
  .intestation{
    display: flex;
    flex-direction: column;
    align-items: center;
    row-gap: 30px;
    h4{
      text-transform: uppercase;
      font-size: 40px;
      font-weight: normal;
    }
  }
  .component-container{
    padding: 100px 0;
    margin: 0 80px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
</style>
