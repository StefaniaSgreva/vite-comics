<template>
    <section class="dark">
        <div class="wrapper">
            Content goes here
        </div>
    </section>
</template>

<script>
    export default {
        name: 'DarkContentSection',
    }
</script>

<style lang="scss" scoped>
    @use '../assets/styles/partials/mixins' as *;
    @use '../assets/styles/partials/variables' as *;
    .dark{
        height: 130px;
        background-color: $black;
        color: $white;
        @include dflex;
    }
</style>