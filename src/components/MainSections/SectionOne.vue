<script>
export default {
    
}
</script>
<template lang="">
    <div>
        <div class="main-cont">
            <div class="p-cont">
                <div class="deco">

                </div>
                <div class="main-p">
                    <p>
                        Let passion and determination be guide along the way and develop at your own place that's comfortable.
                    </p>
                    <div class="author">
                        Fannie Moreno
                    </div>
                    <div class="mansion">
                        /Founder & CEO
                    </div>
                </div>
                <div class="deco">

                </div>
            </div>
            <div class="number-cont">
                <div class="number-section">
                    <div class="number">
                        1.926
                    </div>
                    <div class="details">
                        FINISHED SESSIONS
                    </div>
                </div>
                <div class="number-section">
                   <div class="number">
                    3.092+
                    </div>
                    <div class="details">
                        ENROLLED LEARNERS
                    </div> 
                </div>
                <div class="number-section">
                   <div class="number">
                        200
                    </div>
                    <div class="details">
                        ONLINE INSTRUCTORS
                    </div> 
                </div>
                <div class="number-section">
                   <div class="number">
                    100%
                    </div>
                    <div class="details">
                        SATISFACTION RATE
                    </div> 
                </div>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    .main-cont{
        width: 80%;
        margin: 0 auto;
        height: 500px;
        margin-top: 100px;
        .p-cont{
            width: 100%;
            height: 80%;
            display: flex;
            align-items: center;
            justify-content: space-between;
            .deco{
                width: 20%;
            }
            .main-p{
                width: 40%;
                text-align: center;
                color: rgb(53, 53, 53);
                p{
                    font-size: x-large;
                    font-weight: bold;
                }
                .author{
                    padding-top: 50px;
                }
                .mansion{
                    color: darkgray;
                    font-size: small;
                }
            }
        }
        .number-cont{
            width: 80%;
            margin: 0 auto;
            height: 20%;
            display: flex;
            .number-section{
                width: 25%;
                height: 100%;
                display: flex;
                flex-direction: column;
                align-items: center;
                justify-content: center;
                .number{
                    color: rgb(38, 221, 151);
                    font-size: xx-large;
                    font-weight: bold;
                }
                .details{
                    font-size: x-small;
                    color: rgb(53, 53, 53);
                    margin-top: 10px;
                }
            }
        }
    }
</style>