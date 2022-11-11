<template>
    <div class="footer-links">
        <ul>
            <h4>{{item.title}}</h4>
            <li v-for="(link,index) in item.links" :key="index"><a :href="link.url">{{link.text}}</a></li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'FooterMenu',
        props: [
            'item'
        ]
    }
</script>

<style lang="scss" scoped>

</style>