<script>
import Jumbotron from './components-section/Jumbotron.vue';
import OurConsultation from './components-section/OurConsultation.vue';

export default {
    name: 'MainApp',
    components: {
        Jumbotron,
        OurConsultation,
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

    <section id="about-us">
        <div class="container">
            <div class="left">Lorem.</div>
            <div class="right">
                <div class="section">
                    <hr>
                    <span>ABOUT US</span>
                </div>
                <h1>WE MAKE YOUR STRATEGY WORK</h1>
                <p>
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nam distinctio voluptas veniam, qui rem
                    corrupti quo eos quisquam reiciendis dolor.
                </p>
            </div>
            <div class="banner">
                <div class="left_banner">
                    <span>Lorem ipsum dolor sit.</span>
                </div>
                <div class="right_banner">
                    <p>Lorem ipsum dolor sit.</p>

                </div>
                <button>get started</button>
            </div>
        </div>

    </section>
    <!-- /#about-us -->

    <section id="project">
        <div class="container">
            <div class="section">
                <hr>
                <span>PROJECT</span>
            </div>
            <div class="header-project">
                <h1>OUR EXPERT TRUSTED CONSULTANTS HELP CLIENTS</h1>
                <div class="btn-prev-next">
                    <button>prev</button>
                    <button>next</button>
                </div>
            </div>
            <div class="row">
                <div class="col-3">Lorem, ipsum.</div>
                <div class="col-3">Dolores, quisquam?</div>
                <div class="col-3">Fugit, nemo?</div>
            </div>

        </div>
    </section>
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
