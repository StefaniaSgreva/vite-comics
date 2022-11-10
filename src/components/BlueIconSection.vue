<template>
    <section class="menu-icons">
        Icons
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
    }
</style>