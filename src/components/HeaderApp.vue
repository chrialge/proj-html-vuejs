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
      <div class="navbar">
        <ul>
          <li v-for="section in navbar"><a :href="section.href">{{ section.name }}</a></li>
        </ul>
      </div>
      <!-- /navbar -->

    </nav>
  </header>
  <!-- site-header -->

</template>

<style></style>
