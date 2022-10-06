<template>
    <div class="bg-img">
        <div class="component-container">
        <div class="intestation">
            <h4>change a life today</h4>
            <div class="line-warning"></div>
            <span class="font-20">As long as poverty, inijustice & inequality persist, none of us can truly rest. It doesen't take much to change a life. Get in touch today and start making the difference</span>
            <div class="d-flex justify-content-center gap-5">
                <button type="button" class="btn btn-outline-light">volunteer</button>
                <button type="button" class="btn btn-outline-light">donate now</button>
            </div>
        
        </div>
    </div>
    </div>
</template>

<script>
export default {
    name:'SubsciptionComponent'
}
</script>

<style lang="scss" scoped>
    @import '@/style/Variables-Color.scss';
    .bg-img{
        height: 570px;
        display: flex;
        align-items: center;
        justify-content: center;
        background-image: url(@/assets/img/home-footer.jpg);
        background-position-y: center;
        color: $white;
        span{
            color: $white;
            width: 55%;
            text-align: center;
        }
    }
</style>