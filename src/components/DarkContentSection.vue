<template>
    <section class="comics">
        <div class="wrapper">
            <h2>Current Series</h2>
            <div class="row">
                <CurrentSeries v-for="(item,index) in comics" :key="index" :obj="item"/>
            </div>
        </div>
        <button class="load-more">Load More</button>
    </section>
</template>

<script>
    import {dcComics} from '../data/dc-comics.js';
    import CurrentSeries from './CurrentSeries.vue';
    export default {
        name: 'DarkContentSection',
        components: {
            CurrentSeries,
        },
        data(){
            return {
                comics: dcComics,
            }
        },
        mounted(){
            console.log(this.comics);
        }
    }
</script>

<style lang="scss">
    @use '../assets/styles/partials/mixins' as *;
    @use '../assets/styles/partials/variables' as *;

    .comics{
        background-color: $black;
        color: $white;
        position: relative;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        h2{
            background-color: $blue;
            padding: 1rem 2rem;
            position: absolute;
            top: -2rem;
        }
        .row{
            @include dflex;

            .col{
                align-self: flex-start;
                width: calc(100% / 6);
                padding: 2rem .75rem;
                
                .img-container{
                    width: 185px;
                    height: 185px;
                    overflow: hidden;
                }

                h4{
                    text-align: center;
                    margin-top: 1rem;
                }
            }
        }

        .load-more{
            background-color: $blue;
            color: $white;
            padding: .75rem 3.5rem;
            margin-bottom: 1.3rem;
        }
    }
</style>