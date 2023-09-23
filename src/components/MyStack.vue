<template>
    <div class="mystack-main">
        <h1>{{ mystackTitle }}</h1>
        <div class="stack-content">
            <div class="stack-container" v-for="(name, index) in names" :key="index">
                <img class="svg-imgs" :src="svg_imgs[index]" :alt="names[index]">
                <p>{{ names[index] }}</p>
            </div>
        </div>
    </div>
</template>

<script>
    export default{
        name: 'MyStack',
        props: {
            names: {
                type: Array,
                required: true
            },
            svg_imgs: {
                type: Array,
                required: true
            },
            mystackTitle: String,
        }
    }
</script>

<style lang="scss" scoped>
@import '../assets/scss/MyStack.scss';
</style>