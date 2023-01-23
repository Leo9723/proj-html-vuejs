<script>
export default {
    
}
</script>
<template lang="">
    <div class="all">
    <div class="jumbo-cont">
        <h1>
            Learn At Your Own Place!
        </h1>
        <p>
            Get teamed up with people of same will.
        </p>
        <button>
            Get started for free
        </button>
        <div class="wave-cont">
            <div class="media-cont">
            <img src="/public/images/home-6-hero-left-person-244x300.png" alt="" class="left-person-img">
            <div class="video-cont">
                <div class="poster">
                <img src="/public/images/home-6-hero-poster-final.jpg" alt="">
                </div>
                <img src="/public/images/icon-youtube-play.png" alt="" class="yt">
            </div>
            <img src="/public/images/home-6-hero-right-person-195x300.png" alt="" class="right-person-img">
            </div>
        </div>
    </div>
    </div>
</template>
<style lang="scss" scoped>
.all{
    background-color: #1f1f52;
    color: white;
    .jumbo-cont{
        display: flex;
        flex-direction: column;
        align-items: center;
        h1, p, button, .media-cont{
            margin-top: 50px;
        }
        h1{
            font-size: 50px;
        }
        p{
            color: rgb(168, 168, 168);
        }
        button {
            padding: 15px 30px;
            color: white;
            font-weight: bold;
            background-color: rgb(74, 209, 157);
            border: none;
            border-radius: 10px;
            box-shadow: 0px 0px 30px 5px rgba(63, 63, 63, 0.911);
        }
        .wave-cont{
            width: 100%;
            background-image: url(../../public/images/wave\ -3.svg), url(../../public/images/wave\ -2.svg), url(../../public/images/wave\ -1.svg);
            background-size: cover;
            .media-cont{
                width: 80%;
                margin: 0 auto;
                display: flex;
                justify-content: space-between;
                .right-person-img{
                    position: relative;
                    top: 250px;
                }
                .left-person-img{
                    position: relative;
                    top: 90px;
                }
                .video-cont{
                        background-color: white;
                        box-shadow: 0px 0px 30px 5px rgba(114, 114, 114, 0.384);
                        border-radius: 15px;
                        position: relative;
                        top: 50px;
                        right: 20px;
                        height: 460px;
                        width: 760px;
                        display: flex;
                        align-items: center;
                        justify-content: center;
                        .poster{
                            overflow: hidden;
                            img{
                                transition: all 1.0s;
                                &:hover{
                                    transform: scale(1.2);
                                }
                        }
                        }
                        .yt{
                            position: absolute;
                            left: 50%;
                            top: 50%;
                            transform: translate(-50%, -50%);
                        }
                }
            }
        }
        
    }
}
</style>