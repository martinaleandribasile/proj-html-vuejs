<template>
 <div class="header">
  <NavbarComponent/>
  <div class="box-header">
    <h1 class="header-title">MAKE A DIFFERENCE</h1>
    <p class="sub-title">As long as poverty, injustice & inequality persist, none of us can truly rest</p>
    <div class="header-button">
      <button type="button" class="btn btn-outline-light">our mission</button>
      <button type="button" class="btn btn-outline-warning">donate now</button>
    </div>
  </div>
 </div>
</template>

<script>
  import NavbarComponent from '@/components/NavbarComponent.vue'
export default {
  name: "HeaderComponent",
  components: {
    NavbarComponent
  }
}
</script>


<style scoped lang="scss">
  .header{
    color: white;
    background-image: url(@/assets/img/home-page-slider.jpg);
    background-size: cover;
    background-position-y: 25%;
    height: 900px;
    .box-header{
      height: 80%;
      display: flex;
      flex-direction: column;
      row-gap: 15px;
      align-items: center;
      justify-content: center;
      .header-title{
        font-size: 90px;
        transform: scaleY(0.9);
        font-weight: normal;
        text-transform: uppercase;
        word-spacing: 0.8rem;
      }
      .sub-title{
          font-size: 20px;
          font-weight: 100;
          word-spacing: 0.1rem;
        }
       
        .header-button{
          display: flex;
          flex-direction: row;
          gap: 20px;
        }
    }
  }
</style>
