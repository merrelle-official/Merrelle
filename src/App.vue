<template>
  <div class="mhead">
    <div class="head-list">
      <MHead :itemCount="4" :linkText="['hello', 'aboutme', 'mystack', 'projects']" :menuText="['Hello', 'About me','My Stack', 'Projects']"></MHead>
    </div>
  </div>

  <div class="main">
    <section id="hello"></section>
    <MainInfo class="allinfo" :job_title="jobTitle" :surname="surname" :name="name" :age="age" :photo_url="photos_url" :tg_link="myTg" :git_link="myGitHub"></MainInfo>
    <section id="aboutme"></section>
    <AboutMe class="allaboutme" :value="aboutmeValue" :title="aboutmeTitle" :titleofblock="aboutmeBlockTitle" :textofblock="aboutmeBlockText"></AboutMe>
    <section id="mystack"></section>
    <MyStack class="allmystack" :names="stackNames" :svg_imgs="stackSvg" :mystackTitle="stackTitle"></MyStack>
    <section id="projects"></section>
    <MyProjects class="allmyproj" :title="projTitle" :count_of_projects="projCount" :projName="projNames" :projDescription="projDescriptions" :projLinks="projIsLink" :projGit="projIsGit" :projImg="projImgs"></MyProjects>
  </div>
  <MyFooter class="footer"></MyFooter>



</template>

<script>
// Подключённые компоненты
import MHead from "./components/Head.vue"
import MainInfo from "./components/MainInfo.vue"
import AboutMe from "./components/AboutMe.vue"
import MyStack from "./components/MyStack.vue"
import MyProjects from "./components/MyProjects.vue"
import MyFooter from "./components/Footer.vue"

// Мои фотографии
import Img1 from "./assets/img/1.jpg"

// Мой стек технологий
import html_svg from "./assets/img/html5.svg"
import css_svg from "./assets/img/css3.svg"
import js_svg from "./assets/img/javascript.svg"
import tp_svg from "./assets/img/typescript.svg"
import scss_svg from "./assets/img/scss.svg"
import bootstrap_svg from "./assets/img/bootstrap.svg"
import react_svg from "./assets/img/react.svg"
import vue_svg from "./assets/img/vue.svg"

// Мои проекты
import h2ions_png from "./assets/img/h2ions.png"

export default {
  name: 'App',
  components: {
    MHead,
    MainInfo,
    AboutMe,
    MyStack,
    MyProjects,
    MyFooter
  },
  data() {
    return {
      myGitHub: "https://github.com/merrelle-official",
      myTg: "https://t.me/kuroisuns",
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
      "Обычно всё свободное время я трачу на развитие в профессиональной области, смотрю различные видио, читаю статьи на Habr, ищу новые способы вёрстки и структурирования информации на странице, но помимо этого увлекаюсь просмотром фильмов/сериалов/аниме и играми"],
      stackNames: ["HTML5", "CSS3", "JavaScript", "TypeScript", "SCSS", "Bootstrap", "React", "Vue"],
      stackSvg: [html_svg, css_svg, js_svg, tp_svg, scss_svg, bootstrap_svg, react_svg, vue_svg],
      stackTitle: "Мой Стек",
      projTitle: "Проекты",
      projCount: 1,
      projNames: ["H2IONS"],
      projDescriptions: ["Вёрстка пользовательского интерфейса медицинского оборудования для планшетов"],
      projIsLink: [0],
      projIsGit: [0],
      projImgs: [h2ions_png]

    }
  }
}
</script>

<style lang="scss">
@import './assets/scss/App.scss';
</style>
