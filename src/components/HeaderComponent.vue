<template>
    <header>
        <div class="wrapper">
            <a href="#" class="header-logo">
                <img src="../assets/img/dc-logo.png" alt="DC Header Logo">
            </a>
            <nav>
                <ul>
                    <li v-for="(link,index) in headerLinks" :key="index">
                        <a :href="link.url" :class="{'active' : link.current}">{{link.text}}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
    export default {
        name: 'HeaderComponent',
        data(){
            return {
                headerLinks: [
                    {
                        text: "Characters",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Comics",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Movies",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Tv",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Games",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Collectibles",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Videos",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Fans",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "News",
                        url: "#",
                        current: false,
                    },
                    {
                        text: "Shop",
                        url: "#",
                        current: false,
                    },
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
   @use '../assets/styles/partials/mixins' as *;
   @use '../assets/styles/partials/variables' as *;

    header{
        background-color: $white;
        
            .wrapper{
                @include dflex;
                width: 70%;
                margin: 0 auto;
                padding: 1rem 0;
            }
            .header-logo{
                width: 5rem;
            }

            ul{
                list-style: none;
                //  margin: 2.5rem 1rem 4rem;
                 @include dflex;

                 li a{
                    display: inline-block;
                    padding: 1rem;
                    text-decoration: none;
                    text-transform: uppercase;
                    font-size: .85rem;
                    font-weight: 600;
                    color: $black;

                    &.active,
                    &:hover{
                    text-decoration: underline;
                    color: $blue
                }
                 }

            }

    }
</style>