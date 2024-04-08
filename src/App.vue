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
  <h1>{{ msg }}</h1>
  <div>
    <HeaderApp />
    <MainApp />
    <FooterApp />
  </div>
</template>

<style lang="scss"></style>
