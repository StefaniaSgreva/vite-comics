<template>
    <footer>
        <div class="top">
            <div class="wrapper">
                <nav>
                    <div class="R-nav">
                        <ul>
                            <h4>Dc Comics</h4>
                            <li v-for="(link,index) in dcComics" :key="index"><a :href="link.url">{{link.text}}</a></li>
                        </ul>
                        <ul>
                            <h4>Shop</h4>
                            <li v-for="(link,index) in shop" :key="index"><a :href="link.url">{{link.text}}</a></li>
                        </ul>
                    </div>
                    <div class="next-nav">
                        <ul>
                            <h4>Dc</h4>
                            <li v-for="(link,index) in dc" :key="index"><a :href="link.url">{{link.text}}</a></li>
                        </ul>
                        <ul>
                            <h4>Sites</h4>
                            <li v-for="(link,index) in sites" :key="index"><a :href="link.url">{{link.text}}</a></li>
                        </ul>
                    </div>
                </nav>
                <div class="dc-logo-footer">
                    <img src="../assets/img/dc-logo-bg.png" alt="DC Footer Logo">
                </div>
            </div>
        </div>
        <div class="bottom">
            <div class="wrapper">
                <button>Sign-up Now</button>
                <div class="icon-links">
                    <span>Follow Us</span>
                    <a href="#"><img src="../assets/img/footer-facebook.png" alt="facebook link"></a>
                    <a href="#"><img src="../assets/img/footer-twitter.png" alt="twitter link"></a>
                    <a href="#"><img src="../assets/img/footer-youtube.png" alt="YouTube link"></a>
                    <a href="#"><img src="../assets/img/footer-pinterest.png" alt="Pinterest link"></a>
                    <a href="#"><img src="../assets/img/footer-periscope.png" alt="Maps link"></a>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
    export default {
        name: 'FooterComponent',
        data(){
            return {
                dcComics: [
                    {
                        text: "Characters",
                        url: "#",
                    },
                    {
                        text: "Comics",
                        url: "#",
                    },
                    {
                        text: "Movies",
                        url: "#",
                    },
                    {
                        text: "Tv",
                        url: "#",
                    },
                    {
                        text: "Games",
                        url: "#",
                    },
                    {
                        text: "Videos",
                        url: "#",
                    },
                    {
                        text: "News",
                        url: "#",
                    }
                ],
                shop: [
                    {
                        text: "Shop DC",
                        url: "#",
                    },
                    {
                        text: "Shop Dc Collectibles",
                        url: "#",
                    }
                ],
                dc: [
                    {
                        text: "Terms Of Use",
                        url: "#",
                    },
                    {
                        text: "Privacy policy (New)",
                        url: "#",
                    },
                    {
                        text: "Ad Choices",
                        url: "#",
                    },
                    {
                        text: "Advertising",
                        url: "#",
                    },
                    {
                        text: "Jobs",
                        url: "#",
                    },
                    {
                        text: "Subscriptions",
                        url: "#",
                    },
                    {
                        text: "Talent Workshops",
                        url: "#",
                    },
                    {
                        text: "CPSC Certificates",
                        url: "#",
                    },
                    {
                        text: "Ratings",
                        url: "#",
                    },
                    {
                        text: "Shop Help",
                        url: "#",
                    },
                    {
                        text: "Contact Us",
                        url: "#",
                    }
                ],
                sites: [
                    {
                        text: "DC",
                        url: "#",
                    },
                    {
                        text: "MAD Magazine",
                        url: "#",
                    },
                    {
                        text: "DC Kids",
                        url: "#",
                    },
                    {
                        text: "DC Universe",
                        url: "#",
                    },
                    {
                        text: "DC Power Visa",
                        url: "#",
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

footer{
    color: $white;
}
.top{
    height: 370px;
    background-image: url(../assets/img/footer-bg.jpg);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    overflow: hidden;
    
    .wrapper{
        position: relative;
    }
    nav{
        display: flex;
        padding: 2rem 0;

        .R-nav{
            margin-right: 2rem;

            ul:nth-child(2){
                margin-top: 1rem;
            }
        }
        .next-nav{
            display: flex;
            ul{
                margin-right: 2rem;

            }
        }
        li a{
            color: $white;
            opacity: .5;
            font-size: .75rem;

            &:hover{
                    text-decoration: underline;
            }
        }
        h4{
            margin-bottom: 1rem;
        }
    }
    .dc-logo-footer{
        position: absolute;
        right: 0;
        top: -6rem;
    }
}
.bottom{
    padding: 1rem 0;
    background-color: $dark-gray;

    button{
        background-color: transparent;
        border: 2px solid $blue;
        padding: .75rem;
        color: $white;
        text-transform: uppercase;
        font-weight: 600;

    }
    .icon-links{
        display: flex;
        align-items: center;

        img{
            width: 1.5rem;
            margin-left: .75rem;
        }
            span{
            text-transform: uppercase;
            color: $blue;
            font-weight: 600;
            padding-right: .75rem;
        }
    }
    
}
</style>