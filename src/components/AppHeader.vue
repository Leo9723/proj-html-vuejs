<script>
export default {
    data(){
        return {
            HeaderList: [
        {
            title: "Home",
            showMore: false,
            List: [
                "MaxCoach Education",
                "Course Portal",
                "Distant Learning",
                "Multimedia Pedagology",
                "Modern Schooling",
                "Remote Training",
                "Healt Coaching",
                "Gym Coaching",
                "Buisness",
                "Artist",
                "Kitchen",
                "Motivation",
                "Dancing",
                "Guitar",
                "Yoga",
                "Photography",
                "Personal Finance",
                "Sales Coaching",
                "Mental Teraphy"

            ]
        },
        {
            title: "Pages",
            showMore: false,
            List: [
                "Start Here",
                "Success Story",
                "About me",
                "About us 01",
                "About us 02",
                "About us 03",
                "Contact me",
                "Contact us",
                "Purchase Guide",
                "Privacy Policy",
                "Terms of Service"
            ]
        },
        {
            title: "Courses",
            showMore: false,
            List: [
                "Courses Grid 01",
                "Courses Grid 02",
                "Courses Grid 03",
                "Membership Levels",
                "Become a Teacher",
                "Profile",
                "Checkout",
                "Single Layout"
            ]
        },
        {
            title: "Features",
            showMore: false,
            List: [
                "Events",
                "Zoom Meetings"
            ]
        },
        {
            title: "Blog",
            showMore: false,
            List: [
                "Blog Grid",
                "Blog Masonary",
                "Blog Classic",
                "Blog List"
            ]
        },
        {
            title: "Shop",
            showMore: true,
            List: [
                "Shop Left Sidebar",
                "Shop Right Sidebar",
                "Cart",
                "Wishlist",
                "Single Product"
            ]
        },
    ],
        }
    },
    methods: {
        showOptions(flag){
            if(flag == false){
                flag = true
                console.log(flag)
            }
            else{
                flag = false
                console.log(flag)
            }
        }
    }
}
</script>
<template lang="">
    <div class="header-cont">
        <div class="row">
            <div class="logo">
                LOGO
            </div>
            <div class="navbar">
                <ul class="main-list">
                    <li v-for="(name, index) in this.HeaderList" class="main-item">
                        <div class="option" @click="showOptions(name.showMore)">
                        {{ name.title }} V
                        </div>
                        <ul v-if="name.showMore">
                            <li v-for="(item, index) in name.List">{{ item }}</li>
                        </ul>
                    </li>
                    <div class="icon">I-Carr</div>
                    <div class="icon">I-Usr</div>
                </ul>

            </div>
            <div class="searchbar">
                <input type="search" name="" id="">
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    .row {
        width: 70%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        color: white;
        background-color: rgb(75, 3, 134);
        .navbar{
            width: 70%;
            .main-list{
                display: flex;
                justify-content: space-around;
                list-style-type: none;
                .main-item{
                    position: relative;
                }
                ul{
                    list-style-type: none;
                    position: absolute;
                    right: -25%;
                    color: black;
                    background-color: white;
                    border: 1px solid black;
                }
            }
        }
    }
</style>