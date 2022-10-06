<template>
   <div id="JOURNAL">
    <div class="component-container">
        <div class="intestation">
            <h4>latest articles</h4>
            <div class="line-warning"></div>
            <span class="font-20">Togheter we make all the difference</span>
        </div>
        <div class="box-articles">
            <div class="left-box">
                <img src="@/assets/img/photo-1444213007800-cff19e1677ac-600x450.jpg" alt="">
                <div class="px-3">
                    <h5 class="text-color">Understanding community complexities</h5>
                    <span>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eveniet illo totam odio mollitia, eos aspernatur voluptates officiis delectus ad itaque incidunt tempora. </span>
                </div>
            </div>
            <div class="right-box">
                <div class="card-article" v-for="article in articles" :key="article.title">
                    <img :src='require(`@/assets/img/${article.urlimage}.jpg`)' alt="">
                    <div class="card-text">
                        <h5>{{article.title}}</h5>
                        <span>{{article.text}}</span>
                    </div>
                </div>
            </div>
        </div>
        <div class="box-articles">
            <button class="w-100 p-3 button-articles">view all our articles</button>
        </div>
    </div>
    
 </div>
</template>

<script>
export default {
    name:'ArticlesComponent',
    props:{
        articles:Array
    }
}
</script>

<style lang="scss" scoped>
    @import "@/style/Variables-Color.scss";
    @mixin dis-flex-row{
        display: flex;
        flex-direction: row;
    }
    @mixin dis-flex-col{
        display: flex;
        flex-direction: column;
    }
    span{
        color: $dark-grey;
    }
    .component-container{
        row-gap: 60px;
        .box-articles{
            @include dis-flex-row;
            justify-content: space-between;
            width: 80%;
            margin: 0 auto;
            .button-articles{
                border: 0;
                font-size: 20px;
                color: $white;
                background-color: $burt-sienna;
                &:hover{
                    background-color: $burt-sienna-light;
                }
            }
            .left-box{
                border: 1px solid $light-grey;
                height: 650px;
                width: 50%;
                padding-bottom: 10px;
                @include dis-flex-col;
                row-gap: 20px;
                .text-color{
                    color: $ocra;
                    font-weight: normal;
                    font-size: 25px;
                }
            }
            .right-box{
                height: 650px;
                width: 45%;
                padding-bottom: 10px;
                @include dis-flex-col;
                row-gap: 10px;
                .card-article{
                    height: calc(100% / 4);
                    @include dis-flex-row;
                    .card-text{
                        padding-left: 20px;
                        h5{
                            color: $ocra;
                        }
                    }
                } 
            }
        }
    }
 
</style>