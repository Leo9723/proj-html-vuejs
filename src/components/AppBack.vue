<script>
export default {
    
}
</script>
<template lang="">
    <div class="back-button">
        <button>
            <a href="#jumbo-id">
                <i class="fa-solid fa-arrow-up"></i>
            </a>
        </button>
    </div>
</template>
<style lang="scss" scoped>
    @use '../components/styles/partials/variables' as *;

    button {
        padding: 20px 23px;
        border: none;
        border-radius: 100%;
        background-color: $extra-color;
        a{
            text-decoration: none;
            color: white;
        }
    }
</style>