<script>
export default {
    data(){
        return{
            icons: [
                {
                    ico: "fa-solid fa-ruler-combined",
                    text: "Select Demo",
                    url: "https://themeforest.net/item/maxcoach-online-courses-education-wp-theme/26051639"
                },
                {
                    ico: "fa-regular fa-life-ring",
                    text: "Support Channel",
                    url: "https://thememove.ticksy.com/"
                },
                {
                    ico: "fa-solid fa-book",
                    text: "Documentation",
                    url: "https://document.thememove.com/maxcoach/"
                },
                {
                    ico: "fa-solid fa-cart-shopping",
                    text: "Purchase Maxcoach",
                    url: "https://themeforest.net/item/maxcoach-online-courses-education-wp-theme/26051639"
                }
            ],
        }
    }
}
</script>
<template lang="">
    <div class="nav">
        <div class="nav-cont">
            <div class="ico" v-for="(icon, index) in icons">
                <div class="text">{{ icon.text }}</div>
                <!-- creazione quadrato da roteare per fare freccia -->
                <div class="square"></div>
                <a :href="icon.url" :class="(index == 0) ? 'first' : (index == 3) ? 'last' : ''"><i :class="icon.ico"></i></a>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../components/styles/partials/variables' as *;
.nav{
    position: fixed;
    top: 20%;
    left: 88%;
    z-index: 5;
}
    .nav-cont{
        border-radius: 5px 0px 0px 5px;
        .ico{
            display: flex;
            align-items: center;
            &:hover .text, &:hover .square {
                opacity: 1;
            }
            &:hover .text{
                left: 10px;
            }
            &:hover .square{
                left: 0px;
            }
            .text{
                width: 150px;
                font-size: small;
                padding: 8px;
                margin: 2px 0px 2px 0px;
                color: white;
                background-color: black;
                border-radius: 5px;
                opacity: 0;
                transition: all 0.25s;
                position: relative;
                left: 35px;
            }
            a{
                padding: 10px 100px 10px 15px;
                text-decoration: none;
                color: $primary-text;
                background-color: white;
            }
            .first{
                border-radius: 5px 0px 0px 0px;
            }
            .last{
                border-radius: 0px 0px 0px 5px;
            }
            .square {
                width: 15px;
                height: 15px;
                background-color: black;
                position: relative;
                left: 25px;
                right: 0px;
                rotate: 45deg;
                border-radius: 5px;
                opacity: 0;
                transition: all 0.20s;
            }
        }
    }
</style>