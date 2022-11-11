<template>
    <footer>
        <div class="top">
            <div class="wrapper">
                <nav>
                    <div class="R-nav">
                        <FooterMenu v-for="(menu,index) in navBarsR" :key="index" :item="menu"/>
                    </div>
                    <div class="next-nav">
                        <FooterMenu v-for="(menu,index) in navBarsL" :key="index" :item="menu"/>
                    </div>
                </nav>
                <div class="dc-logo-footer">
                    <img src="../assets/img/dc-logo-bg.png" alt="DC Footer Logo">
                </div>
            </div>
        </div>
        <div class="bottom">
            <div class="wrapper">
                <button>Sign-up Now!</button>
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
    import {footerMenuR} from '../data/dc-comics.js';
    import {footerMenuL} from '../data/dc-comics.js';
    import FooterMenu from './FooterMenu.vue';
    export default {
        name: 'FooterComponent',
        components:{
            FooterMenu
        },
        data(){
            return {
                navBarsR: footerMenuR, 
                navBarsL: footerMenuL,
            }
        }
    }
</script>

<style lang="scss">
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
            margin-top: -1rem;

            

            ul{
                margin-top: 1rem;
            }
           
        }
        .next-nav{
            display: flex;
            margin-top: -1rem;

            ul{
                margin-top: 1rem;
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
            font-size: 1.2rem;
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
        cursor: pointer;
        font-size: 1.1rem;
    }
    .icon-links{
        display: flex;
        align-items: center;

        img{
            width: 2rem;
            margin-left: 1rem;
        }
            span{
            text-transform: uppercase;
            color: $blue;
            font-size: 1.2rem;
            font-weight: 600;
            margin-right: .75rem;
        }
    }
    
}
</style>