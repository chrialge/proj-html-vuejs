<script>
import Jumbotron from './components-section/Jumbotron.vue';
import OurConsultation from './components-section/OurConsultation.vue';
import AboutUs from './components-section/AboutUs.vue';
import Project from './components-section/Project.vue';
import Testimonial from './components-section/Testimonial.vue';
import Blog from './components-section/Blog.vue'
import Banner from './components-section/Banner.vue'

export default {
    name: 'MainApp',
    components: {
        Jumbotron,
        OurConsultation,
        AboutUs,
        Project,
        Testimonial,
        Blog,
        Banner,
    },
    data() {
        return {
            msg: 'main'
        }
    }
}
</script>

<template>

    <main id="sitemain">

        <Jumbotron />
        <!-- /#jumbotron -->

        <OurConsultation />
        <!-- /#our-consultation -->

        <AboutUs />
        <!-- /#about-us -->

        <Project />
        <!-- /#project -->

        <Testimonial />
        <!-- /#testimonial -->

        <Blog />
        <!-- /#blog -->

        <Banner />
        <!-- /#banner -->
        
    </main>
    <!-- /#sitemain -->


</template>

<style></style>
