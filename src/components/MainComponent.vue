<template>
  <div class="main">
   <MomentComponent/>
   <ValueComponent :values='values'/>
   <CausesComponent :listimg='listimg'/>
   <ArticlesComponent :articles='articles'/>
   <SubsciptionComponent/>
  </div>
</template>

<script>
    import MomentComponent from '@/components/MainComponentsFile/MomentComponent.vue'
    import ValueComponent from '@/components/MainComponentsFile/ValueComponent.vue'
    import CausesComponent from '@/components/MainComponentsFile/CausesComponent.vue'
    import ArticlesComponent from '@/components/MainComponentsFile/ArticlesComponent.vue'
    import SubsciptionComponent from '@/components/MainComponentsFile/SubsciptionComponent.vue'
    import {values} from '@/filesData/valuesComponent.js'
    import {listimg} from "@/filesData/listimg.js"
    import {articles} from "@/filesData/articles.js"
export default {
name:'MainComponent',
data(){
    return {
        values,
        listimg,
        articles,
    }
},
components:{
    MomentComponent,
    ValueComponent,
    CausesComponent,
    ArticlesComponent,
    SubsciptionComponent
}
}
</script>

<style lang="scss" scoped>

</style>