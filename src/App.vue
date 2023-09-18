<template>
  <div class="mhead">
    <div class="head-list">
      <MHead :itemCount="4" :linkText="['hello', 'aboutme', 'mystack', 'projects']" :menuText="['Hello', 'About me','My Stack', 'Projects']"></MHead>
    </div>
  </div>

  <div class="main">
    <section id="hello"></section>
    <MainInfo class="allinfo" :job_title="jobTitle" :surname="surname" :name="name" :age="age" :photo_url="photos_url"></MainInfo>
    <section id="aboutme"></section>
    <AboutMe class="allaboutme" :value="aboutmeValue" :title="aboutmeTitle" :titleofblock="aboutmeBlockTitle" :textofblock="aboutmeBlockText"></AboutMe>
  </div>



</template>

<script>
import MHead from "./components/Head.vue"
import MainInfo from "./components/MainInfo.vue"
import AboutMe from "./components/AboutMe.vue"

import Img1 from "./assets/img/1.jpg"

export default {
  name: 'App',
  components: {
    MHead,
    MainInfo,
    AboutMe,
  },
  data() {
    return {
      jobTitle: "Frontend-разработчик",
      surname: "Чернышев",
      name: "Владимир",
      age: "21 год",
      photos_url: Img1,
      aboutmeValue: 3,
      aboutmeTitle: "Обо мне",
      aboutmeBlockTitle: ["Кто я",
      "Почему Fronted",
      "Свободное время"],
      aboutmeBlockText: ["Frontend-разработчик из Москвы, оканчиваю последний курс в Московском Государственном Психолого-Педагогическом Университете (МГППУ), сейчас активно развиваюсь в сфере web-разработки, ищу способы развития и профессионального роста",
      "У меня всегда была тяга к кодингу, но одновременно с этим и к разработке визуального оформления пользовательских интерфейсов, Backend-разработка и написание скриптов таких возможностей не предоставляло, поэтому я решил, что Frontend для меня лучший выбор, в чём я и убедился, начав активно развиваться в этой области",
      "Обычно всё свободное время я трачу на развитие в профессиональной области, смотрю различные видио, читаю статьи на Habr, ищу новые способы вёрстки и структурирования информации на странице, но помимо этого увлекаюсь просмотром фильмов/сериалов/аниме и играми"]
    }
  }
}
</script>

<style lang="scss">
@import './assets/scss/App.scss';
</style>
