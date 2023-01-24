<script>
export default {
    data(){
        return {
            activeOption: 7,
            HeaderList: [
        {
            title: "Home",
            url:"https://maxcoach.thememove.com/",
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
                "Sales Coaching"
            ]
        },
        {
            title: "Pages",
            url:"https://maxcoach.thememove.com/",
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
            url:"https://maxcoach.thememove.com/main/courses/",
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
            url:"https://maxcoach.thememove.com/main/courses/",
            List: [
                "Events",
                "Zoom Meetings"
            ]
        },
        {
            title: "Blog",
            url:"https://maxcoach.thememove.com/main/blog/",
            List: [
                "Blog Grid",
                "Blog Masonary",
                "Blog Classic",
                "Blog List"
            ]
        },
        {
            title: "Shop",
            url:"https://maxcoach.thememove.com/main/shop/",
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
                        <div class="option">
                        <a :href="name.url">{{ name.title }} V</a>
                        </div>
                        <ul :class="(name.List.length > 15) ? 'split-ul-15' : (name.List.length > 7) ? 'split-ul-10' : ''">
                            <li v-for="(item, num) in name.List" :class="(name.List.length > 7) ? 'split-li-15' : ''">{{ item }}</li>
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
    .header-cont{
        background-color: #1f1f52;
        height: 50px;
    }
    .row {
        height: 100%;
        width: 70%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        color: white;
        .navbar{
            width: 70%;
            .main-list{
                display: flex;
                justify-content: space-around;
                list-style-type: none;
                .main-item{
                    position: relative;
                    a{
                     text-decoration: none;
                     color: white;
                     }
                    &:hover ul{
                        top: 20px;
                        opacity: 1;
                    }
                }
                .split-ul-15 {
                    height: 300px;
                    width: 450px;
                    display: flex;
                    flex-direction: column;
                    flex-wrap: wrap;
                    right: -150%;
                }
                .split-ul-10{
                    height: 200px;
                    width: 450px;
                    display: flex;
                    flex-direction: column;
                    flex-wrap: wrap;
                    right: -150%;
                }
                ul{
                    list-style-type: none;
                    position: absolute;
                    right: -25%;
                    top: 30px;
                    color: black;
                    opacity: 0;
                    transition: all 0.5s;
                    z-index: 2;
                    background-color: white;
                    border-radius: 15px;
                    .split-li-15 {
                        height: 50px;
                        width: 150px;
                    }
                    li{
                        padding: 5px;
                        height: 50px;
                        width: 100px;
                    }
                }
            }
        }
    }
</style>