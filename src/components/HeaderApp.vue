<script>
export default {
  name: 'HeaderApp',
  data() {
    return {
      msg: 'header',
      navbar:[
        {name:'HOME', href:'#jumbotron'},
        {name:'ABOUT', href:'#about-us'},
        {name:'PROJECTS', href:'#projects'},
        {name:'SERVICES', href:'#testimonials'},
        {name:'BLOG', href:'#blog'},
        {name:'CONTACT', href:'#site-footer'}
      ]
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
