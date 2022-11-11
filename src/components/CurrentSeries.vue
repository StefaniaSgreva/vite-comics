<template>
    <div class="col">
        <div class="img-container">
            <img :src="obj.thumb" :alt="obj.series">
        </div>
        <h4>{{obj.series}}</h4>
    </div>
</template>

<script>
    export default {
        name: 'CurrentSeries',
        props: [
            'obj'
        ]
    }
</script>

<style lang="scss" scoped>

</style>