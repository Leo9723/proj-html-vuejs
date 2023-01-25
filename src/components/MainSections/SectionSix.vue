<script>
export default {
    data(){
        return{
            cards: [
                {
                    ico: "fa-regular fa-flag",
                    title:"Idea Discussion",
                    paragraph: "Get teamed up with the specialists who work and teach coding for years at famous universities."
                },
                {
                    ico: "fa-solid fa-gear",
                    title:"Web Development",
                    paragraph: "Learn to start building o webpage from scratch. You decide your own pace, course and speed."
                },
                {
                    ico: "fa-regular fa-life-ring",
                    title:"System Administration",
                    paragraph: "Learners are encouragad to study the mechonism ond structure of system administration."
                },
                {
                    ico: "fa-solid fa-display",
                    title:"Graphic Design",
                    paragraph: "Have a passion for graphics and arts? Snow your talents with confidence and self-assertiveness."
                }
            ],
            scroll: false
        }
    },
    methods: {
        activescroll(){
            this.scroll = true
        }
    },
}
</script>
<template lang="">
    <div @mouseover="activescroll" :class="(this.scroll) ? 'all mouse-over' : 'all'">
        <div class="main-cont">
            <div class="intestation">
                <div class="info">
                    WANNA TRANSFORM YOUR LIFE?
                </div>
                <h2>Glad to <span>Help You</span> Learn</h2>
            </div>
            <div class="cards">
                <div class="card" v-for="card in cards">
                    <i :class="card.ico"></i>
                    <h3>{{ card.title }}</h3>
                    <p>{{ card.paragraph }}</p>
                </div>
            </div>
            <img src="/public/images/home-6-services-image.png" alt="">
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
.all.mouse-over {
        transition: all 2s;
        opacity: 1;
        top: 0px;
    }
    .all{
        background-image: linear-gradient($bkg-main-primary, $bkg-main-secondary);
        opacity: 0;
        position: relative;
        top: 50px;
    }
        .main-cont{
        width: 80%;
        margin: 0 auto;
        padding-top: 50px;
        img{
            position: relative;
            top: 35px;
        }
        .intestation{
            text-align: center;
            padding-bottom: 50px;
        }
        .info{
            font-size: small;
            color: $secondary-text;
        }
        h2{
            font-size: 40px;
            margin: 20px 0px;
            span{
                font-weight: lighter;
                color: $extra-color;
            }
        }
        .cards{
            display: flex;
            justify-content: space-between;
            margin-bottom: 150px;
            .card{
                width: calc(90% / 4);
                i{
                    font-size: xx-large;
                }
                h3{
                    margin: 15px 0px;
                    font-size: 20px;
                }
                p{
                    color: $secondary-text;
                    line-height: 1.7;
                }
            }
        }
    }
</style>