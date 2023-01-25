<script>
export default {
    data(){
        return{
            scroll: false,
            numberOne: 0,
            numberOneStatic: "1.926",
            numberTwo: 0,
            numberTwoStatic: "3.092",
            numberThree: 0,
            numberThreeStatic: "200",
            numberFour: 0,
            numberFourStatic: "100",
            interval: 0,
        }
    },
    methods: {
        activescroll(){
            this.scroll = true
        },
        updateTimer() {
            if(this.scroll){
                clearInterval(this.interval)
                this.interval = setInterval(()=>{
                  if(this.numberOne < 100){
                      this.numberOne = this.numberOne + 1
                      this.numberTwo = this.numberTwo + 1
                      this.numberThree = this.numberThree + 1
                      this.numberFour = this.numberFour + 1
                  }
                }, 13)

            }
      }
    },
    computed: {
      myVal() {
            let self = this;
                this.updateTimer()
                if(this.numberOne < 100){
                    return this.numberOne
                }
                else {
                    return this.numberOneStatic
                }
      },
      myValTwo() {
        let self = this;
            this.updateTimer()
            if(this.numberTwo < 100){
                return this.numberTwo
            }
            else {
                return this.numberTwoStatic
            }
      },
      myValThree() {
        let self = this;
            this.updateTimer()
            if(this.numberThree < 100){
                return this.numberThree
            }
            else {
                return this.numberThreeStatic
            }
      },
      myValFour() {
        let self = this;
            this.updateTimer()
            if(this.numberFour < 100){
                return this.numberFour
            }
            else {
                return this.numberFourStatic
            }
      }
  },
}
</script>
<template lang="">
    <div>
        <div @mouseover="activescroll" :class="(this.scroll) ? 'main-cont mouse-over' : 'main-cont'">
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
                        {{ myVal }}
                    </div>
                    <div class="details">
                        FINISHED SESSIONS
                    </div>
                </div>
                <div class="number-section">
                   <div class="number">
                    {{ myValTwo }}+
                    </div>
                    <div class="details">
                        ENROLLED LEARNERS
                    </div> 
                </div>
                <div class="number-section">
                   <div class="number">
                        {{ myValThree }}
                    </div>
                    <div class="details">
                        ONLINE INSTRUCTORS
                    </div> 
                </div>
                <div class="number-section">
                   <div class="number">
                    {{ myValFour }}%
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
@use '../styles/partials/variables' as *;
    .main-cont.mouse-over {
        transition: all 2s;
        opacity: 1;
        top: 0px;
    }
    .main-cont{
        width: 80%;
        margin: 0 auto;
        height: 500px;
        margin-top: 100px;
        padding-bottom: 50px;
        opacity: 0;
        position: relative;
        top: 50px;
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
                p{
                    font-size: x-large;
                    font-weight: bold;
                }
                .author{
                    padding-top: 50px;
                }
                .mansion{
                    color: $secondary-text;
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
                    color: $extra-color;
                    font-size: xx-large;
                    font-weight: bold;
                }
                .details{
                    font-size: x-small;
                    color: $secondary-text;
                    margin-top: 10px;
                }
            }
        }
    }
</style>