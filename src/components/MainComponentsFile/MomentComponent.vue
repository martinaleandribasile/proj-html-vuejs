<template>
<div id="MISSION" >
    <div class="moments-container">
        <div class="moments-par">
            <h3 class="moment-title">every moment counts</h3>
            <div class="w-25 line-warning"></div>
            <p>Curabitur non mi et turpis pharetra vulpate. Cras consequat, risus nec commodo vehicula, nisi et laoreet leo, ac convallis nisi nibh id velit. Aliquam mattis metus a nisi pretium</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem repudiandae facilis natus quasi officiis perspiciatis labore illum unde accusantium quos animi, repellat voluptas, delectus molestias veniam commodi sapiente assumenda non.</p>
            <p>Curabitur non mi et turpis pharetra vulpate. Cras consequat, risus nec commodo vehicula, nisi et laoreet leo, ac convallis nisi nibh id velit.</p>
            <button class="w-25 btn btn-warning text-white">our mission</button>
        </div>
        <div class="moments-statisctics ">
           <div v-for="component in info "  :key="component.text" >
                <div class="statistic" >
                <i :class="component.icon"></i>
                <span >{{component.number}} <span v-if="component.numberText">{{component.numberText}}</span></span>
                </div>
                <p>{{component.text}}</p>
           </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name:'MomentComponent',
    data(){
        return{
            info:[
                {
                    icon: "fa-regular fa-heart",
                    text:'Volunteers worldwide',
                    number: 2032,
                },
                {
                    icon: "fa-solid fa-globe",
                    text:'Active projects',
                    number: 132,
                },
                {
                    icon: "fa-solid fa-dollar-sign",
                    text:'Donate',
                    number: 3.8,
                    numberText:'M',
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '@/style/Variables-Color.scss';
    @mixin dis-flex-col{
        display: flex;
        flex-direction: column;
    }
    .moments-container{
        display: flex;
        flex-direction: row;
        .moments-par{
            width: 65%;
            margin-left: 80px;
           @include dis-flex-col;
            padding: 5% 10% 5% 0;
            row-gap: 20px;
            .moment-title{
                text-transform: uppercase;
                font-weight: normal;
                font-size: 40px;
                transform: scaleY(0.9);
                word-spacing: 0.3rem;
            }
            p{
                color: $dark-grey;
            }
            .line-warning{
                height: 5px;
                background-color: $ocra;
            }
        }
        .moments-statisctics{
            background-image: url(@/assets/img/home-content-bg-1.jpg);
            background-size: 100%;
            background-position: center;
            background-repeat: repeat;
            @include dis-flex-col;
            align-items: center;
            justify-content: space-evenly;
            width: 35%;
            color: $white;
            .statistic{
                font-size: 40px;
                display: flex;
                align-items: center;
                justify-content: center;
                gap: 10px; 
            }
            p{
                text-align: center;
            }
        }
    }
</style>