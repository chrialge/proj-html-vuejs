<script>
import HeaderApp from './components/HeaderApp.vue';
import MainApp from './components/MainApp.vue';
import FooterApp from './components/FooterApp.vue';

export default {
  name: app,
  data() {
    return {
      msg: 'bella'
    }
  },
  components: {
    HeaderApp,
    MainApp,
    FooterApp
  },
}
</script>
<template>


  <HeaderApp />
  <MainApp />
  <FooterApp />

  <div class="actions d-flex">
    <div class="page-up">
      <a href="#">
        <i class="fa-solid fa-arrow-up-long"></i>
      </a>
    </div>
    <div class="chat">
      <a href="#">
        <i class="fa-regular fa-comment"></i>
      </a>
    </div>
  </div>

</template>

<style lang="scss"></style>
