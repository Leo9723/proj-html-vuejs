<script>
export default {
    data(){
        return{
            cards: [
                {
                    title: "Graphic Design",
                    paragraph: "Have a passion for graphics and arts? Show your talents with confidence ond self-assertiveness.",
                    img: "home-6-service-image-01.png" 
                },
                {
                    title: "Idea Discussion",
                    paragraph: "Gat teamed up with the specialists who work and teach coding for years at famous universities.",
                    img: "home-6-service-image-03.png"
                },
                {
                    title: "Buisness Administration",
                    paragraph: "Leorners are encouraged ta study the mechanism and structure of system administratiom.",
                    img: "home-6-service-image-02.png"
                },
                {
                    title: "Web Development",
                    paragraph: "Learn to start building a webpage from scratch. You decide your own pace. course and speed.",
                    img: "home-6-service-image-04.png"
                }
            ],
            Check:[
                "Select & customize courses to your preferences",
                "Change the tutor and make arrangements",
                "Porticipate in events to join others",
                "Get the desired certificate delivered at house"
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
    <div>
        <div @mouseover="activescroll" :class="(this.scroll) ? 'main-cont mouse-over' : 'main-cont'">
            <div class="cards-cont">
                <div v-for="(card, index) in cards" :class="(index > 1) ? 'cards down' : 'cards'">
                    <div :class="(index == 1) ? 'card reverse' : (index == 3) ? 'card reverse' : 'card'">
                        <div class="card-text">
                            <h3>{{ card.title }}</h3>
                            <p>{{ card.paragraph }}</p>
                        </div>
                        <img :src="`/public/images/`+ card.img" alt="">
                    </div>
                </div>
            </div>
            <div class="check-cont">
                <div class="intro">
                    TOGETHER WE CAN CREATE
                </div>
                <h2>Service We <span>Can Provide</span> For My Clients.</h2>
                <div class="check"  v-for="(item, num) in Check">
                    <i class="fa-solid fa-check"></i> {{ item }}
                </div>
                <button>
                    Get started for free
                </button>
            </div>
        </div>

    </div>
</template>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
    .main-cont.mouse-over {
        transition: all 2s;
        opacity: 1;
        top: 0px;
    }
    .main-cont{
        width: 80%;
        margin: 0 auto;
        display: flex;
        justify-content: space-around;
        opacity: 0;
        position: relative;
        top: 50px;
        .cards-cont{
            width: 50%;
            display: flex;
            flex-direction: column;
            flex-wrap: wrap;
            height: 1000px;
            .down {
                position: relative;
                top: 40px;
            }
            .cards{
                width: 40%;
                margin-top: 30px;
                margin-right: 30px;
                min-height: 380px;
                box-shadow: 0px 0px 30px 5px rgba(114, 114, 114, 0.384);
                .card{
                    display: flex;
                    flex-direction: column;
                    justify-content: space-between;
                    height: 100%;
                    h3{
                        margin: 15px;
                    }
                    p{
                        margin: 15px;
                        font-size: small;
                        line-height: 1.5;
                        color: $secondary-text;
                    }
                    img {
                        width: 200px;
                        margin-left: 15px;
                    }
                }
                .reverse{
                    flex-direction: column-reverse;
                    img{
                        margin-top: 15px;
                    }
                }
            }
        }
        .check-cont{
            width: 30%;
            align-self: center;
            .intro{
                font-size: x-small;
                margin-bottom: 20px;
            }
            h2{
                font-size: 35px;
                margin-bottom: 40px;
                span{
                    color: $extra-color;
                    font-weight: lighter;
                }
            }
            .check{
                line-height: 2;
                i{
                    color: $extra-color;
                }
            }
            button{
                margin-top: 30px;
                @include my-button;
                &:hover{
                    @include my-hover-button-2;
                }
            }
            
        }
    }
</style>