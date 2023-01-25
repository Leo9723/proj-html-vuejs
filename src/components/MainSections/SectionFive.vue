<script>
export default {
    data(){
        return{
            cards: [
                {
                    img: "artist-blog-03-480x325.jpeg",
                    title: "Brush Strokes Energize Trees in Paintings",
                    date: "May 15, 2020",
                    views: "688"
                },
                {
                    img: "artist-blog-01-480x325.jpg",
                    title: "Pocket-Sized Notebooks Hold Miniature Paintings",
                    date: "May 15, 2020",
                    views: "603"
                },
                {
                    img: "artist-blog-02-480x325.jpg",
                    title: "Connection Between Self-Portraits and Identity",
                    date: "May 15, 2020",
                    views: "397"
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
                <div class="intro">
                    ENJOY READING ON MAXCOACH
                </div>
                <h2>Latest on <span>Our Blogs</span></h2>
            </div>
            <div class="cards">
                <div class="card"  v-for="card in cards">
                    <div class="img">
                        <img :src="`/public/images/` + card.img" alt="">
                    </div>
                    <div class="intro">
                        ARTIST
                    </div>
                    <h3>{{ card.title }}</h3>
                    <div class="card-info">
                    <div class="date">
                        <i class="fa-regular fa-calendar"></i> {{ card.date }}
                    </div>
                    <div class="views">
                        <i class="fa-regular fa-eye"></i> {{ card.views }}
                    </div>
                    </div>
                </div>
            </div>
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
        background-color: $bkg-main-secondary;
        padding: 50px 0px;
        opacity: 0;
        position: relative;
        top: 50px;
    }
    .main-cont{
        width: 80%;
        margin: 0 auto;
        .intestation{
            text-align: center;
        }
        .intro{
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
            .card{
                width: calc(90% / 3);
                .img{
                    overflow: hidden;
                    width: 368px;
                    height: 249px;
                    border-radius: 10px;
                }
                img{
                    width: 100%;
                    border-radius: 10px;
                    margin-bottom: 15px;
                    transition: all 1.5s;
                    &:hover{
                        transform: scale(1.2);
                    }
                }
                h3{
                    margin: 15px 0px;
                }
                .card-info{
                    display: flex;
                    font-size: small;
                    color: $secondary-text;
                    .views{
                        margin-left: 20px;
                    }
                }
            }
        }

    }
</style>