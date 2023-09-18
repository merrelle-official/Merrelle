<template>
    <div class="aboutme-main">
        <div class="aboutme-title"><h1>{{ title }}</h1></div>
        <div v-for="(item, index) in value" :key="index" class="main-blocks">
            <div :class="{ 'left-text': index % 2 === 0, 'right-text': index % 2 !== 0 }">
                <div class="block-text">
                    <h1>{{ titleofblock[index] }}</h1>
                    <p>{{ textofblock[index] }}</p>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    export default{
        name: 'AboutMe',
        props: {
            value: {
                type: Number,
                default: 1
            },
            title: {
                type: String,
                required: true
            },
            titleofblock: {
                type: Array,
                required: true
            },
            textofblock: {
                type: Array,
                required: true
            },
        }
    }
</script>
<style lang="scss" scoped>
@import '../assets/scss/AboutMe.scss';

</style>