<template>
    <section class="menu-icons">
        <div class="wrapper">
            <div class="digital-comics">
                <img src="../assets/img/buy-comics-digital-comics.png" alt="Digital Comics">
                <span>Digital Comics</span>
            </div>
            <div class="merciandise">
                <img src="../assets/img/buy-comics-merchandise.png" alt="DC Merciandise">
                <span>DC Merciandise</span>
            </div>
            <div class="subscriptions">
                <img src="../assets/img/buy-comics-subscriptions.png" alt="Subscriptions">
                <span>Subscriptions</span>
            </div>
            <div class="shop-locator">
                <img src="../assets/img/buy-comics-shop-locator.png" alt="Shop Locator">
                <span>Comic Shop Locator</span>
            </div>
            <div class="power-visa">
                <img src="../assets/img/buy-dc-power-visa.svg" alt="DC Power Visa">
                <span>DC Power Visa</span>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'BlueIconSection',
    }
</script>

<style lang="scss" scoped>
    @use '../assets/styles/partials/mixins' as *;
    @use '../assets/styles/partials/variables' as *;
    .menu-icons{
        height: 153px;
        background-color: $blue;
        color: $white;
        @include dflex;

        div{
            display: flex;
            justify-content: space-around;
            align-items: center;
        }
        img{
            width: 3.2rem;
            margin-right: 1rem;
        }
        .digital-comics img{
            width: 2.7rem;

        }
        .shop-locator img{
            width: 2.1rem;

        }
        span{
            text-transform: uppercase;
            font-size: .75rem;
        }
    }
</style>