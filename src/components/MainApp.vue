<script>
import Jumbotron from './components-section/Jumbotron.vue';
import OurConsultation from './components-section/OurConsultation.vue';
import AboutUs from './components-section/AboutUs.vue'
import Project from './components-section/Project.vue'

export default {
    name: 'MainApp',
    components: {
        Jumbotron,
        OurConsultation,
        AboutUs,
        Project,
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

    <section id="testimonial">
        <div class="container">
            <div class="container_header">
                <div class="section">
                    <span>testimonial</span>
                    <hr>
                </div>
                <h1>WHAT'S THE CUSTOMER SAY ABOUT OUR WORK</h1>
            </div>
            <div class="container_testimonials">
                <div class="testimonials">
                    <div class="testimonial col-3">
                        <p>
                            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Voluptatibus voluptates, delectus
                            nesciunt odio debitis commodi blanditiis quo accusamus quos laboriosam.
                        </p>
                        <h5>
                            Lorem, ipsum.
                        </h5>
                        <span>Lorem.</span>
                    </div>
                    <div class="testimonial col-3">
                        <p>
                            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Voluptatibus voluptates, delectus
                            nesciunt odio debitis commodi blanditiis quo accusamus quos laboriosam.
                        </p>
                        <h5>
                            Lorem, ipsum.
                        </h5>
                        <span>Lorem.</span>
                    </div>
                    <div class="testimonial col-3">
                        <p>
                            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Voluptatibus voluptates, delectus
                            nesciunt odio debitis commodi blanditiis quo accusamus quos laboriosam.
                        </p>
                        <h5>
                            Lorem, ipsum.
                        </h5>
                        <span>Lorem.</span>
                    </div>
                </div>
            </div>

        </div>

    </section>
    <!-- /#testimonial -->

    <section id="blog">
        <div class="container">
            <div class="section">
                <hr>
                <span>BLOG</span>
            </div>
            <div class="header-blog">
                <h1>THE RECENT NEWS YOU MUST READ IT</h1>
                <button>view all</button>
            </div>
            <div class="row">
                <div class="img col-2">
                    <div class="banner-img">Lorem, ipsum dolor.</div>
                </div>
                <div class="img col-2">
                    <div class="banner-img">Lorem, ipsum dolor.</div>
                </div>
            </div>


        </div>
    </section>
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
