<template>
    <footer>
        <div class="top">
            nav
        </div>
        <div class="bottom">
            links
        </div>
    </footer>
</template>

<script>
    export default {
        name: 'FooterComponent',
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;


.top{
    height: 370px;
    background-image: url(../assets/img/footer-bg.jpg);
}
.bottom{
    height: 110px;
    background-color: $dark-gray;
}
</style>