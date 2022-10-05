<template>
 <div id="CAUSES">
    <div class="value-container">
        <div class="value-intestation">
            <h4>RECENT CAUSES</h4>
            <div class="line-warning"></div>
            <span>We run projects in over 30 countries in 5 continents</span>
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
    .value-container{
        padding: 100px 0;
        margin: 0 80px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        .value-intestation{
            display: flex;
            flex-direction: column;
            align-items: center;
            row-gap: 30px;
            .line-warning{
                width: 180px;
                height: 5px;
                background-color: #fcd66c;
            }
            h4{
                font-size: 40px;
                font-weight: normal;
            }
            span{
                font-size: 20px;
            }
        }
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
        background-color: #ed6864;
        color: white;
        text-transform: uppercase;
        display: flex;
        justify-content: center;
        align-items: center;
    }

</style>