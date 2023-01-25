<script>
export default {
    data(){
        return{
            cards: [
                {
                    img: "course-02-480x298.jpg",
                    money: "40",
                    title: "Learninf to Write a Professional Author",
                    lessonsNumber: "20",
                    studentsNumber: "",
                    free: false
                },
                {
                    img: "stock-full-hd-04-480x298.jpg",
                    money: "19",
                    title: "Open Programming Courses for Everyone: Python",
                    lessonsNumber: "17",
                    studentsNumber: "62",
                    free: false
                },
                {
                    img: "course-featured-image-01-480x298.jpg",
                    money: "39",
                    title: "Master jQuery in a Short Period of Time",
                    lessonsNumber: "6",
                    studentsNumber: "51",
                    free: false
                },
                {
                    img: "stock-full-hd-03-480x298.jpg",
                    money: "Free",
                    title: "Customer-centric Info-Tech Strategies",
                    lessonsNumber: "24",
                    studentsNumber: "769",
                    free: true
                },
                {
                    img: "stock-full-hd-06-480x298.jpg",
                    money: "26",
                    title: "Academic Listening and Note-taking",
                    lessonsNumber: "14",
                    studentsNumber: "67",
                    free: false
                },
                {
                    img: "stock-full-hd-05-480x298.jpg",
                    money: "59",
                    title: "Introduction to Javascript for Beginners",
                    lessonsNumber: "14",
                    studentsNumber: "67",
                    free: false
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
    <div>
        <div @mouseover="activescroll" :class="(this.scroll) ? 'main-cont mouse-over' : 'main-cont'">
            <div class="intro">
                CHOOSE A COURSE TO GET STARTED
            </div>
            <h2 class="title">
                Latest Featured <span>Courses</span>
            </h2>
            <div class="cards">
                <div class="card" v-for="(card, index) in cards">
                    <img :src="`/public/images/` + card.img" alt="">
                    <div class="info">
                        <div class="money" v-if="card.free == true">
                            {{ card.money }}
                        </div>
                        <div class="money" v-else>
                            ${{ card.money }}<span>.00</span>
                        </div>
                        <div class="title">
                            {{ card.title }}
                        </div>
                        <div class="statistics">
                            <div class="lessons">
                                <i class="fa-regular fa-file-lines"></i> {{ card.lessonsNumber }} Lessons
                            </div>
                            <div class="students">
                                <i class="fa-regular fa-user"></i> {{ card.studentsNumber }} Students
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <button>View all courses <i class="fa-solid fa-arrow-right"></i></button>
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
    text-align: center;
    background-color: $bkg-main-secondary;
    padding-top: 50px;
    opacity: 0;
    position: relative;
    top: 50px;
}
.intro{
    font-size: small;
    color: $secondary-text;
}
h2{
    font-size: 40px;
    margin-bottom: 50px;
    span{
        font-weight: lighter;
        color: $extra-color;
    }
}
button{
    margin-top: 50px;
    @include my-button;
    margin-bottom: 50px;
    &:hover{
        @include my-hover-button-2
    }
}
.cards{
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    height: 700px;
    width: 80%;
    margin: 0 auto;
    text-align: start;
}
    .card{
        display: flex;
        height: 180px;
        margin-bottom: 20px;
        margin: 20px;
        padding: 10px;
        transition: all 0.25s;
        border-radius: 10px;
        &:hover{
            background-color: $bkg-main-primary;
            box-shadow: 0px 0px 30px 5px rgba(114, 114, 114, 0.384);
        }
        img{
            width: 160px;
            aspect-ratio: 1 / 1;
            object-fit: cover;
            border-radius: 100%;
        }
        .info{
            margin-left: 30px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            .money{
                font-size: large;
                font-weight: bold;
                color: $extra-color;
                margin-bottom: 15px;
                span{
                    font-size: small;
                }
            }
            .title{
                font-weight: bold;
                line-height: 1.7;
            }
            .statistics{
                display: flex;
                margin-top: 30px;
                color: $secondary-text;
                .lessons{
                    margin-right: 40px;
                }
            }
        }
    }
</style>