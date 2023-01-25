<script>
export default {
    data(){
        return{
            cards: [
                {
                    ico: "ico",
                    title:"Idea Discussion",
                    paragraph: "Get teamed up with the specialists who work and teach coding for years at famous universities."
                },
                {
                    ico: "ico",
                    title:"Web Development",
                    paragraph: "Learn to start building o webpage from scratch. You decide your own pace, course and speed."
                },
                {
                    ico: "ico",
                    title:"System Administration",
                    paragraph: "Learners are encouragad to study the mechonism ond structure of system administration."
                },
                {
                    ico: "ico",
                    title:"Graphic Design",
                    paragraph: "Have a passion for graphics and arts? Snow your talents with confidence and self-assertiveness."
                }
            ]
        }
    }
}
</script>
<template lang="">
    <div class="main-cont">
        <div class="intestation">
            <div class="info">
                WANNA TRANSFORM YOUR LIFE?
            </div>
            <h2>Glad to <span>Help You</span> Learn</h2>
        </div>
        <div class="cards">
            <div class="card" v-for="card in cards">
                <div :class="card.ico">ICONA</div>
                <h3>{{ card.title }}</h3>
                <p>{{ card.paragraph }}</p>
            </div>
        </div>
        <img src="/public/images/home-6-services-image.png" alt="">
    </div>
</template>
<style lang="scss" scoped>
        .main-cont{
        width: 80%;
        margin: 0 auto;
        margin-top: 50px;
        .intestation{
            text-align: center;
        }
        .intro{
            font-size: small;
            color: gray;
        }
        h2{
            font-size: 40px;
            margin: 20px 0px;
            span{
                font-weight: lighter;
                color: rgb(88, 241, 183);
            }
        }
        .cards{
            display: flex;
            justify-content: space-between;
            margin-bottom: 150px;
            .card{
                width: calc(90% / 4);
                h3{
                    margin: 15px 0px;
                    font-size: 20px;
                }
                p{
                    color: gray;
                    line-height: 1.7;
                }
            }
        }
    }
</style>