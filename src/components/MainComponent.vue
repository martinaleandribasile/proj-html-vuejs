<template>
  <div class="main">
   <MomentComponent/>
   <ValueComponent :values='values'/>
  </div>
</template>

<script>
    import MomentComponent from '@/components/MomentComponent.vue'
    import ValueComponent from '@/components/ValueComponent.vue'
    import {values} from '@/valuesComponent.js'
export default {
name:'MainComponent',
data(){
    return {
        values
    }
},
components:{
    MomentComponent,
    ValueComponent,
}
}
</script>

<style lang="scss" scoped>

</style>