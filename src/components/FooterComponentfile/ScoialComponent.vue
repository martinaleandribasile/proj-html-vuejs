<template>
  <div class="bg-color">
    <div class="component-container py-4 gap-4">
        <span class="copyright"> @ Copyright 2012 - 2020 AVADA THEME BY THEME FUSION  |  ALL RIGHT RESERVED  |  POWERED BY WORDPRESS</span>
        <div class="icons-social">
            <a target="_blank" href="https://it-it.facebook.com/"><i class="fa-brands fa-facebook icona"></i></a>
            <a target="_blank" href="https://www.instagram.com/"><i class="fa-brands fa-instagram icona"></i></a>
            <a target="_blank" href="https://twitter.com/login?lang=it"><i class="fa-brands fa-twitter icona "></i></a>
            <a target="_blank" href="https://www.youtube.com/?hl=it"><i class="fa-brands fa-youtube icona"></i></a>  
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name:"SocialComponent"
}
</script>

<style lang="scss" scoped>
    .bg-color{
        background-color: #e7e7e9;
        .copyright{
            color: #ababab;
            font-size: 10px;
        }
        .icons-social{
            display: flex;
            column-gap: 15px;
            a{
                color: #fcd66c;
                .icona{
                padding: 10px;
                background-color: white;
                border-radius: 50%;
                font-size: 30px;
                }
            }
           
        }
    }
</style>