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
            ]
        }
    }
}
</script>
<template lang="">
    <div>
        <div class="main-cont">
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
                                ico {{ card.lessonsNumber }} Lessons
                            </div>
                            <div class="students">
                                ico {{ card.studentsNumber }} Students
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
.cards{
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    height: 600px;
    width: 80%;
    margin: 0 auto;
}
    .card{
        display: flex;
        height: 180px;
        margin-bottom: 20px;
        img{
            width: 180px;
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
                color: rgb(52, 224, 167);
                margin-bottom: 15px;
            }
            .title{
                font-weight: bold;
                line-height: 1.7;
            }
            .statistics{
                display: flex;
                margin-top: 30px;
                color: rgb(139, 139, 139);
                .lessons{
                    margin-right: 40px;
                }
            }
        }
    }
</style>