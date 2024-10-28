<script>
export default {
  name: 'HeaderApp',
  data() {
    return {
      msg: 'header',

    }
  },
  props: {
    navbar: Array,
  },
  methods: {
    openSiderbar() {
      document.getElementById("overlay").style.visibility = "visible"
      document.getElementById("overlay").style.opacity = 1;
    },
    closeSiderbar() {
      document.getElementById("overlay").style.visibility = ""
      document.getElementById("overlay").style.opacity = '';
    }
  }
}
</script>

<template>
  <!-- site-header -->
  <header id="site_header">
    <nav>
      <!-- logo -->
      <div class="logo">
        <img src="../../public/images/logotype.png" alt="">
      </div>
      <!-- /logo -->

      <!-- navbar -->
      <div class="navbar" >
        <ul>
          <li v-for="section in navbar"><a :href="section.href">{{ section.name }}</a></li>
        </ul>
      </div>
      <!-- /navbar -->

      <div class="sidebar-mobile">
        <i class="fa-solid fa-bars" @click="openSiderbar()"></i>
        <div class="overlay" id="overlay">
          <i class="fa fa-close" aria-hidden="true" @click="closeSiderbar()"></i>
          <ul>
            <li v-for="section in navbar"><a :href="section.href">{{ section.name }}</a></li>
          </ul>
        </div>
      </div>

    </nav>
  </header>
  <!-- site-header -->

</template>

<style></style>
