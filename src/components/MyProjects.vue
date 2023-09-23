<template>
    <div class="myproj-main">
        <h1 class="title">{{ title }}</h1>
        <div class="proj-container">
            <div class="proj-cont" v-for="index in count_of_projects" :key="index">
                <div class="proj">
                    <img class="proj-img" :src="projImg[index - 1]" alt="Картинка отсутствует">
                    <p class="proj-name">{{ projName[index - 1] }}</p>
                    <p class="proj-desc">{{ projDescription[index - 1] }}</p>
                    <div class="buttons">
                        <button :class="{ activelink: projLinks[index - 1] !== 0, inactivelink: projLinks[index - 1] === 0 }" @click="linkClick(projLinks[index - 1])">Посмотреть вживую</button>
                        <button :class="{ activegit: projGit[index - 1] !== 0, inactivegit: projGit[index - 1] === 0 }" @click="gitClick(projGit[index - 1])">Посмотреть код</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
 export default{
    name: "MyProjects",
    props: {
        title: String,
        count_of_projects: Number,
        projName: {
            type: Array
        },
        projDescription: {
            type: Array
        },
        projLinks: {
            type: Array
        },
        projGit: {
            type: Array
        },
        projImg: {
            type: Array
        }
    },
    methods: {
        linkClick(projLinks) {
            if(projLinks !== 0){
                window.open(projLinks, '_blank');
            }
        },
        gitClick(projGit) {
            if(projGit !== 0){
                window.open(projGit, '_blank');
            }
        }
    }
 }
</script>

<style lang="scss" scoped>
@import '../assets/scss/MyProjects.scss';
</style>