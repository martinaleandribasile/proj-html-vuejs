<template>
    <div class="header-navbar">
        <div class="logo-navbar">
            <img src="@/assets/img/avada-charity-logo-retina.png" alt="">
        </div>
        <div class="container-link">
            <a @click="changeActiveLink(index)" :class="link.active? 'text-warning' : 'text-white'" v-for="(link,index) in linkNavbar" :key="link.name" :href=link.link+link.name>{{link.name}}</a>
            <button class="btn btn-warning text-white">donate</button>
        </div>
    </div>
  
</template>

<script>
export default {
name: 'NavbarComponent',
data(){
    return{
        linkNavbar:[
            {
                name:'HOME',
                link:'#',
                active:true
            },
            {
                name:'MISSION',
                link:'#',
                active:false
            },
            {
                name:'CAUSES',
                link:'#',
                active:false
            },
            {
                name:'JOURNAL',
                link:'#',
                active:false
            }
        ]
    }
},
methods:{
    changeActiveLink(i){
        this.linkNavbar.forEach((element,index)=>{
            if(index===i){
                element.active=true
            }else{
                element.active=false
            }
        })
    }
}
}
</script>

<style lang="scss" scoped>
.header-navbar{
    margin: 0 80px;
    height: 20%;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content:space-between;
    
    .logo-navbar{
        height: 40%;
        img{
            height: 100%;
        }
    }

    .container-link{
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        gap: 60px;
        a{
            text-decoration: none;
            display: flex;
            align-items: center;
        }
        button:hover{
            transform: scale(1.1);
        }
    }
}
</style>