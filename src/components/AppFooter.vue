<script>
export default {
    data(){
        return{
            infos: [
                {
                    address: "382 NE 191st St # 87394 Miamir FL 33179-3899",
                    number: "+1(305)547-9909 (9am - spm EST, Monday - Friday)",
                    mail: "support@maxcoach.com",
                    socialIco: [
                        "fa-brands fa-square-facebook",
                        "fa-brands fa-twitter",
                        "fa-brands fa-instagram",
                        "fa-brands fa-linkedin"
                    ]
                }
            ],
            lists: [
                {
                    title: "Explore",
                    items: [
                        {
                            title: "Start here",
                            url: "https://maxcoach.thememove.com/main/start-here/"
                        },
                        {
                            title: "Blog",
                            url: "https://maxcoach.thememove.com/main/blog/"
                        },
                        {
                            title: "About us",
                            url: "https://maxcoach.thememove.com/main/about-us-01/"
                        },
                        {
                            title: "Success story",
                            url: "https://maxcoach.thememove.com/main/success-story/"
                        },
                        {
                            title: "Courses",
                            url: "https://maxcoach.thememove.com/main/courses/"
                        },
                        {
                            title: "Contact us",
                            url: "https://maxcoach.thememove.com/main/contact-us/"
                        }
                    ]
                },
                {
                    title: "Information",
                    items: [
                        {
                            title: "Membership",
                            url: "https://maxcoach.thememove.com/main/wp-login.php?redirect_to=https%3A%2F%2Fmaxcoach.thememove.com%2Fmain%2Fmembership-account%2F"
                        },
                        {
                            title: "Purchase guide",
                            url: "https://maxcoach.thememove.com/main/purchase-guide/"
                        },
                        {
                            title: "Privacy policy",
                            url: "https://maxcoach.thememove.com/main/privacy-policy/"
                        },
                        {
                            title: "Terms of services",
                            url: "https://maxcoach.thememove.com/main/terms-of-service/"
                        }
                    ]
                },
            ]
        }
    }
}
</script>
<template lang="">
    <div class="all">
    <div class="container">
        <div class="info" v-for="info in infos">
            <h4>Address</h4>
            <div class="address">
                {{ info.address }}
            </div>
            <div class="number">
                {{ info.number }}
            </div>
            <div class="mail">
                {{ info.mail }}
            </div>
            <div class="icons">
                <i :class="ico" v-for="ico in info.socialIco"></i>
            </div>
        </div>
        <div class="more">
            <ul class="main-ul">
                <li v-for="list in lists" class="main-li">
                    <h4>{{ list.title }}</h4>
                    <ul>
                        <li v-for="item in list.items">
                            <a :href="item.url">{{ item.title }}</a>
                        </li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>
        <div class="copyright">
            © 2020 Maxcoach. All Rights Reserved
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use './styles/partials/variables' as *;
    .all{
        background-color: $bkg-main-secondary;
        padding-top: 50px;
    }
    .container {
        width: 80%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        .info{
            line-height: 2;
            color: $secondary-text;
            h4{
                color: $primary-text;
            }
            .mail{
                margin-bottom: 15px;
            }
            .icons{
                display: flex;
                i{
                    margin-right: 20px;
                    font-size: x-large;
                    transition: all 0.15s;
                    cursor: pointer;
                    &:hover {
                            color: $extra-color;
                        }
                }
            }
        }
        .more{
            line-height: 2;
            ul{
                list-style-type: none;
            }
            .main-ul{
                display: flex;
                .main-li{
                    width: 250px;
                    ul{
                        height: 110px;
                        display: flex;
                        flex-direction: column;
                        flex-wrap: wrap;
                        color: $secondary-text;
                        font-size: small;
                        li{
                            a{
                                text-decoration: none;
                                color: $secondary-text;
                                &:hover {
                                color: $extra-color;
                            }
                        }
                        }
                    }

                }
            }

        }
    }
    .copyright{
            font-size: small;
            color: $secondary-text;
            padding: 50px 0px;
            text-align: center;
        }
</style>