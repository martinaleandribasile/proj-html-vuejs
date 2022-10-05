<template>
  <div class="main">
   <MomentComponent/>
   <ValueComponent :values='values'/>
   <CausesComponent :listimg='listimg'/>
  </div>
</template>

<script>
    import MomentComponent from '@/components/MomentComponent.vue'
    import ValueComponent from '@/components/ValueComponent.vue'
    import CausesComponent from '@/components/CausesComponent.vue'
    import {values} from '@/filesData/valuesComponent.js'
    import {listimg} from "@/filesData/listimg.js"
export default {
name:'MainComponent',
data(){
    return {
        values,
        listimg
    }
},
components:{
    MomentComponent,
    ValueComponent,
    CausesComponent,
}
}
</script>

<style lang="scss" scoped>

</style>