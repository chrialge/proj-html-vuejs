<script>
export default {
  name: 'HeaderApp',
  data() {
    return {
      msg: 'header'
    }
  }
}
</script>

<template>
  <!-- site-header -->
  <header id="site_header">
    <nav>
      <!-- left -->
      <div class="logo">
        <img src="../../public/images/logotype.png" alt="">
      </div>

      <!-- right -->
      <div class="right">
        <ul>
          <li><a href="#jumbotron">HOME</a></li>
          <li><a href="#about-us">ABOUT</a></li>
          <li><a href="#project">PROJECTS</a></li>
          <li><a href="#testimonials">SERVICES.</a></li>
          <li><a href="#blog">BLOG</a></li>
          <li><a href="#site_footer">CONTACT</a></li>
        </ul>
      </div>
    </nav>
  </header>
  <!-- site-header -->

</template>

<style></style>
