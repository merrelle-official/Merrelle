<template>
    <div v-for="index in itemCount" :key="index" @click="handleDivClick">
        <a class="tag" :href="'#' + linkText[index - 1]">{{ menuText[index - 1] }}</a>
    </div>
</template>

<script>
    export default{
        name: 'HeaderList',
        props: {
            itemCount: {
                type: Number,
                required: true,
            },
            menuText: {
                type: Array,
                required: true,
            },
            linkText: {
                type: Array,
                required: true,
            }
        },
        methods: {
            handleDivClick(event) {
            const link = event.target.querySelector('a');
                if (link) {
                    link.click();
                }
            },
        },
    }
</script>

<style lang="scss" scoped>
@import '../assets/scss/Head.scss';
</style>