<template>
    <header>
        <div class="wrapper">
            <a href="#" class="header-logo">
                <img src="../assets/img/dc-logo.png" alt="DC Header Logo">
            </a>
            <nav>
                <ul>
                    <div class="border" v-for="(link,index) in headerLinks" :key="index" :class="{'active' : link.current}">
                        <li>
                            <a :href="link.url" :class="{'active' : link.current}">{{link.text}}</a>
                        </li>
                    </div>
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
                        current: true,
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
                padding: 0;
            }
            .header-logo{
                width: 5rem;
            }

            ul{
                @include dflex;
                .border{
                    border-bottom: 5px solid transparent;
                    padding: 2rem 0;

                    &.active,
                    &:hover{
                        border-bottom: 5px solid $blue;
                        color: $blue;
                    }

                    li a{
                        display: inline-block;
                        padding: 1rem;
                        text-transform: uppercase;
                        font-size: .85rem;
                        font-weight: 600;
                        color: $black;

                        &.active,
                        &:hover{
                            color: $blue;
                        }
                    }
                }  
                  
        }

    }
</style>