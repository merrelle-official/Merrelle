<template>
  <div class="mhead">
    <div class="head-list">
      <MHead :itemCount="4" :linkText="['hello', 'aboutme', 'mystack', 'projects']" :menuText="['Hello', 'About me','My Stack', 'Projects']"></MHead>
    </div>
  </div>

  <div class="main">
    <MainInfo :job_title="jobTitle" :surname="surname" :name="name" :age="age" :photo_url="photos_url"></MainInfo>
    <!-- <img src="./assets/img/avka.png" alt=""> -->
  </div>

</template>

<script>
import MHead from "./components/Head.vue"
import MainInfo from "./components/MainInfo.vue"
export default {
  name: 'App',
  components: {
    MHead,
    MainInfo
  },
  data() {
    return {
      jobTitle: "Frontend-разработчик",
      surname: "Чернышев",
      name: "Владимир",
      age: "21 год",
      photos_url: "../assets/img/avka.png"

    }
  }
}
</script>

<style lang="scss">
@import './assets/scss/App.scss';
</style>
