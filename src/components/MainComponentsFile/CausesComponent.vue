<template>
 <div id="CAUSES">
    <div class="component-container">
        <div class="intestation">
            <h4>RECENT CAUSES</h4>
            <div class="line-warning"></div>
            <span class="font-20">We run projects in over 30 countries in 5 continents</span>
        </div>
        <div class="box-img">
            <div v-for="img in listimg" :key="img.urlimg">
                <img :src='require(`@/assets/img/${img.urlimg}`)' :alt="img.text">
            </div>
        </div>
    </div>
    <div class="red-cause-view-all">
        <span>view all our causes</span>
    </div>
 </div>
</template>

<script>
export default {
    name:'CausesComponent',
    props:{
        listimg:Array
    }
}
</script>

<style lang="scss" scoped>
    @import '@/style/Variables-Color.scss';
    .component-container{
        .box-img{
            margin-top: 100px;
            display: flex;
            justify-content: space-between;
            width: 100%;
        }
        
    }
    .red-cause-view-all{
        cursor: pointer;
        padding: 50px 0 50px 0;
        background-color: $burt-sienna;
        color: $white;
        text-transform: uppercase;
        display: flex;
        justify-content: center;
        align-items: center;
        &:hover{
            background-color: $burt-sienna-light; 
        }
    }

</style>