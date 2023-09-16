<template>
    <div class="main-myinfo">
        <div class="text-info">
            <p class="job-title">{{ job_title }}</p>
            <p class="name">{{ name }}<br/>{{ surname }}</p>
            <p class="age">{{ age }}</p>
            <div class="git-div">GitHub</div>
            <div class="tg-div">Telegram</div>
        </div>

        <div class="photos">
            <img :src="photo_url" alt="что от">
        </div>
    </div>
</template>

<script>
 export default{
    name: 'MainInfo',
    props: {
        job_title: {
            type: String,
            required: true,
        },
        surname:{
            type: String,
            required: true
        },
        name: {
            type: String,
            required: true,
        },
        age: {
            type: String,
            required: true,
        },
        git_link: {
            type: String,
            required: false,
        },
        tg_link: {
            type: String,
            required: false,
        },
        item_Count: {
            type: Number,
            default: 1,
        },
        photo_url: {
            type: String,
            required: true,
        },
    }
 }
</script>

<style lang="scss" scoped>
@import '../assets/scss/MainInfo.scss';

</style>