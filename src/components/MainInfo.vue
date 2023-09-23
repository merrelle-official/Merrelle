<template>
    <div class="main-myinfo">
        <div class="text-info">
            <p class="job-title">{{ job_title }}</p>
            <div class="name-n-age">
                <p class="name">{{ name }}<br/>{{ surname }}</p>
                <p class="age">{{ age }}</p>
            </div>
            <div class="contacts">
                <div class="git-div" @click="myContactsClick(git_link)"><p>GitHub</p></div>
                <div class="tg-div" @click="myContactsClick(tg_link)"><p>Telegram</p></div> 
            </div>
        </div>

        <div class="photos">
            <img :src="photo_url" alt="фотография">
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
            type: URL,
            required: true,
        },
    },
        methods: {
            myContactsClick(link) {
                console.log(link);
                window.open(link, '_blank');
            }
        }
 }
</script>

<style lang="scss" scoped>
@import '../assets/scss/MainInfo.scss';

</style>