<script>
export default {
    
}
</script>
<template lang="">
    <div class="chat-button">
        <button>
            <a href="#jumbo-id">
                <i class="fa-solid fa-message"></i>
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
        background-color: rgb(34, 102, 228);
        a{
            text-decoration: none;
            color: white;
        }
    }
</style>