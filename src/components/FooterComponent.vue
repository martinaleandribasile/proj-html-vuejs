<template>
  <div>
    <LogoComponent/>
    <SocialComponent/>
  </div>
</template>

<script>
    import LogoComponent from '@/components/FooterComponentfile/LogoComponent.vue'
    import SocialComponent from '@/components/FooterComponentfile/ScoialComponent.vue'
export default {
    name:'FooterComponent',
    components:{
        LogoComponent,
        SocialComponent,
    }
}
</script>

<style>

</style>