<template>
  <div class="value-container">
    <h4>OUR VALUES</h4>
    <div class="line-warning"></div>
    <span>Think Big.Act Bigger.</span>
    <div class="values-box">
        <div class="values" v-for="value in values" :key="value.title">
            <i :class="value.icon" class="icon"></i>
            <h5>{{value.title}}</h5>
            <span class="text-center">{{value.text}}</span>
            <button class="btn btn-warning w-20 text-white">{{value.button}}</button>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name:'ValueComponent',
    props:{
        values:Array
    }
}
</script>

<style lang="scss" scoped>
.value-container{
    color: white;
    padding: 150px 80px;
    min-height: 800px;
    background-position-y: center;
    background-image: url(@/assets/img/home-content-bg-2.jpg);
    display: flex;
    flex-direction: column;
    row-gap: 20px;
    align-items: center;
    h4{
        font-size: 40px;
        font-weight: normal;
    }
    span{
        font-size: 20px;
        font-weight: lighter;
    }
    .line-warning{
        width: 180px;
        height: 5px;
        background-color: #fcd66c;
    }
    .values-box{
            margin-top: 150px;
            display: flex;
            flex-direction: row;
            flex-wrap: wrap;
            row-gap: 50px;
            .values{
                height: 350px;
                display: flex;
                flex-direction: column;
                align-items: center;
                justify-content: space-between;
                width: calc(100% / 4 - 20px);
                margin: 0 10px;
                .icon{
                    color:#fcd66c;
                    font-size: 70px;
                }
                h5{
                    font-weight: normal;
                }
            }
        }
    
}
</style>