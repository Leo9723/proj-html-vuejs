<script>
export default {
    data(){
        return{
            sponsor: [
                "client-logo-colored-01.png",
                "client-logo-colored-02.png",
                "client-logo-colored-03.png",
                "client-logo-colored-04.png",
                "client-logo-colored-05.png",
                "client-logo-colored-06.png"
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
            <h2>
                Why People Talk About <span>MaxCoach</span>?
            </h2>
            <div class="card">
                <div class="img">
                    <img src="/public/images/testimonial-avata-02.jpg" alt="">
                    <img src="/public/images/maxcoach-shape-05.png" alt="" class="shape">
                </div>
                <div class="info">
                <p>I am free to learn at my own pace, follow my own schedule and choose the subject I like. Great study portal for people like me.</p>
                <div class="author">
                    MINA HOLLACE
                </div>
                <div class="mansion">
                    / FREELANCER
                </div>
                </div>
            </div>
            <div class="sponsors">
                <div class="sponsor" v-for="item in sponsor">
                    <img :src="`/public/images/` + item" alt="">
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
.main-cont.mouse-over {
        transition: all 2s;
        opacity: 1;
        top: 0px;
    }
    .main-cont {
        width: 80%;
        margin: 0 auto;
        text-align: center;
        margin-top: 50px;
        opacity: 0;
        position: relative;
        top: 50px;
        h2{
            font-size: 40px;
            span{
                font-weight: lighter;
                color: $extra-color;
            }
        }
        .card{
            display: flex;
            align-items: center;
            text-align: start;
            width: 50%;
            margin: 0 auto;
            img {
                aspect-ratio: 1 / 1;
                scale: 0.7;
                border-radius: 100%;
            }
            .shape{
                position: absolute;
                right: 56%;
                bottom: 36%;
                z-index: -1;
                scale: 0.5;
            }
            p{
                line-height: 1.5;
                margin-bottom: 20px;
                font-size: large;
            }
            .author{
                font-size: small;
                margin-bottom: 20px;
            }
            .mansion{
                font-size: x-small;
                color: $secondary-text;
            }
        }
        .sponsors{
            display: flex;
            justify-content: center;
            .sponsor{
                margin: 50px;
                display: flex;
                align-items: center;
                transition: all 0.25s;
                &:hover{
                    filter: grayscale(100%);
                }
            }
        }
    }
</style>