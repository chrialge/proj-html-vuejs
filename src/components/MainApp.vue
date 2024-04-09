<script>
import Jumbotron from './components-section/Jumbotron.vue';
import OurConsultation from './components-section/OurConsultation.vue';
import AboutUs from './components-section/AboutUs.vue';
import Project from './components-section/Project.vue';
import Testimonial from './components-section/Testimonial.vue';
import Blog from './components-section/Blog.vue'

export default {
    name: 'MainApp',
    components: {
        Jumbotron,
        OurConsultation,
        AboutUs,
        Project,
        Testimonial,
        Blog,
    },
    data() {
        return {
            msg: 'main'
        }
    }
}
</script>

<template>

    <Jumbotron />
    <!-- /#jumbotron -->

    <OurConsultation/>
    <!-- /#our-consultation -->

    <AboutUs/>
    <!-- /#about-us -->

    <Project/>
    <!-- /#project -->

    <Testimonial/>
    <!-- /#testimonial -->

    <Blog/>
    <!-- /#blog -->

    <section id="banner">
        <div class="info_banner">
            <h1>LET'S TALK ABOUT WORK</h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt, dolor?</p>
            <button>get started</button>
        </div>
    </section>
    <!-- /#banner -->
</template>

<style></style>
