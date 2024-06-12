<script>
export default {
    name: 'Testimonial',
    data() {
        return {
            testimonials: [
                { img: 'oliver-ragfelt-488196-2.jpg', name: 'Vera Duncan' },
                { img: 'oliver-ragfelt-488196-unsplash.jpg', name: 'Oliver Garrison' },
                { img: '12679.jpg', name: 'John Smith' }
            ]
        }
    }
}
</script>

<template>
    <section id="testimonial">
        <div class="container_testimonial">
            <div class="container_header">
                <div class="section d-flex">
                    <span class="col-6 space-letter">TESTIMONIAL</span>
                    <div class="container-separeted col-6">
                        <div class="separeted_small"></div>
                    </div>

                </div>
                <h1>WHAT'S THE CUSTOMER SAY ABOUT OUR WORK</h1>
            </div>
            <div class="container_testimonials">
                <div class="testimonials d-flex">
                    <div class="testimonial col-4 posi-rela d-flex" v-for="testimonial in testimonials">
                        <img class="posi-abso" :src="'/images/' + testimonial.img" alt="">
                        <div class="info-testimonial posi-rela">
                            <p class="paragraph">
                                When, while lovely valley teems with vapour around meand eridian sun strikes the upper
                                impernetraable foliage of my trees, and but a thousand unknow plant are noticed when i
                                hear the buzz of the little.
                            </p>
                            <h4>
                                {{ testimonial.name }}
                            </h4>
                            <span class="paragraph">Amazon inc.</span>
                        </div>

                    </div>
                </div>
            </div>

        </div>

    </section>
</template>

<style></style>