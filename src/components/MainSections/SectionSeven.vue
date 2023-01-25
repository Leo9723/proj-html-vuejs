<script>
export default {
    
}
</script>
<template lang="">
    <div class="main-cont">
        <h3>Start today for getting <span>Online Certification</span></h3>
        <h2>You can be your own guiding star with our help!</h2>
        <button>Get started now</button>
    </div>
</template>
<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
@use '../styles/partials/variables' as *;
.main-cont{
    text-align: center;
    margin-top: 100px;
    h3{
        font-size: 20px;
        span{
            font-weight: lighter;
            color: $extra-color;
        }
    }
    h2{
        font-size: 30px;
    }
    button{
        margin-top: 50px;
        @include my-button;
        margin-bottom: 50px;
        &:hover{
            @include my-hover-button-2
        }
    }
}
</style>