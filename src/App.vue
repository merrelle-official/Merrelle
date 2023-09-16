<template>
  <div class="mhead">
    <div class="head-list">
      <MHead :itemCount="4" :linkText="['hello', 'aboutme', 'mystack', 'projects']" :menuText="['Hello', 'About me','My Stack', 'Projects']"></MHead>
    </div>
  </div>

  <div class="main">

  </div>

</template>

<script>
import MHead from "./components/Head.vue";
export default {
  name: 'App',
  components: {
    MHead
  }
}
</script>

<style lang="scss">
@import './assets/scss/App.scss';
</style>
