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
    }
}
</script>
<template lang="">
    <div class="header-cont">
        <div class="row">
            <div class="logo">
                <img src="/public/images/light-logo.png" alt="">
            </div>
            <div class="navbar">
                <ul class="main-list">
                    <li v-for="(name, index) in this.HeaderList" class="main-item">
                        <div class="option">
                        <a :href="name.url">{{ name.title }} <i class="fa-solid fa-chevron-down"></i></a>
                        </div>
                        <!-- creazione molteplici classi per dimensionare i contenitori in base al numero di elementi nella lista -->
                        <ul :class="(name.List.length > 15) ? 'split-ul-15' : (name.List.length > 7) ? 'split-ul-10' : ''">
                            <li v-for="(item, num) in name.List" :class="(name.List.length > 7) ? 'split-li-15' : ''">{{ item }}</li>
                        </ul>
                    </li>
                    <div class="icon"><a href="https://maxcoach.thememove.com/main/cart/"><i class="fa-solid fa-cart-shopping"></i></a></div>
                    <div class="icon"><a href="https://maxcoach.thememove.com/main/profile/"><i class="fa-solid fa-user"></i></a></div>
                </ul>
            </div>
            <div class="searchbar">
                <input type="search" name="" id="padding-id" placeholder="search...">
                <button><i class="fa-solid fa-magnifying-glass"></i></button>
            </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use './styles/partials/variables' as *;
.icon{
    a{
        color: white;
    }
}
.searchbar{
    display: flex;
    margin-left: 20px;
    button{
        border: none;
        padding: 5px 10px;
        border-radius: 0px 5px 5px 0px;
        background-color: white;
        color: $extra-color;
    }
}
#padding-id{
    padding: 5px 10px;
    border: none;
    border-radius: 5px 0px 0px 5px;
}
.logo{
    img{
        width: 50%;
    }
}
    .header-cont{
        background-color: $bkg-header;
    }
    .row {
        height: 100%;
        width: 70%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
        color: $bkg-main-primary;
        .navbar{
            width: 70%;
            .main-list{
                display: flex;
                justify-content: space-around;
                list-style-type: none;
                .main-item{
                    position: relative;
                    padding-bottom: 10px;
                    border-bottom: 3px solid transparent;
                    i{
                        scale: 0.7;
                    }
                    a{
                     text-decoration: none;
                     color: $bkg-main-primary;
                     }
                     &:hover{
                        border-bottom: 3px solid $bkg-main-primary;
                        border-radius: 2px;
                     }
                    &:hover ul{
                        top: 40px;
                        visibility: visible;
                        opacity: 1;
                        box-shadow: 0px 0px 30px 5px rgba(114, 114, 114, 0.384);
                    }
                    ul{
                        padding: 15px;
                    }
                }
                .split-ul-15 {
                    height: 300px;
                    width: 650px;
                    display: flex;
                    flex-direction: column;
                    flex-wrap: wrap;
                    right: -150%;
                }
                .split-ul-10{
                    height: 200px;
                    width: 650px;
                    display: flex;
                    flex-direction: column;
                    flex-wrap: wrap;
                    right: -150%;
                }
                ul{
                    list-style-type: none;
                    position: absolute;
                    right: -25%;
                    top: 60px;
                    color: $primary-text;
                    visibility: hidden;
                    opacity: 0;
                    transition: all 0.5s;
                    background-color: $bkg-main-secondary;
                    border-bottom: 7px solid $extra-color;
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