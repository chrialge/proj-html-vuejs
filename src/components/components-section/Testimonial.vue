<script>
export default {
    name: 'Testimonial',
    data() {


        return {}
    }
}
</script>

<template>
    <section id="testimonial">
        <div class="container">
            <div class="container_header">
                <div class="section d-flex">
                    <span class="col-6">TESTIMONIAL</span>
                    <div class="container-separeted col-6">
                       <div class="separeted_small"></div> 
                    </div>
                    
                </div>
                <h1>WHAT'S THE CUSTOMER SAY ABOUT OUR WORK</h1>
            </div>
            <div class="container_testimonials">
                <div class="testimonials d-flex">
                    <div class="testimonial col-3" v-for="n in 3">
                        <p class="paragraph">
                            When, while lovely valley teems with vapour around meand eridian sun strikes the upper impernetraable foliage of my trees, and but a thousand unknow plant are noticed when i hear the buzz of the little.
                        </p>
                        <h4>
                            Vera Duncan
                        </h4>
                        <span class="paragraph">Amazon inc.</span>
                    </div>
                </div>
            </div>

        </div>

    </section>
</template>

<style></style>