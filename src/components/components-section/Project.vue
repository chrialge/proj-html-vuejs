<script>
export default {
    name: 'Project',
    data() {
        return {
            images: [
                'DRY-1-790x592.jpg',
                '221bf0b7-8134-43bb-936a-5acbe42db64a-790x592.jpg',
                'z1el4c4p-790x592.jpg'
            ]
        }
    }
}
</script>

<template>
    <section id="project">
        <div class="container">
            <div class="section">
                <div class="separeted_small"></div>
                <span class="space-letter">PROJECT</span>
            </div>
            <div class="header-project d-flex">
                <h1>OUR EXPERT TRUSTED CONSULTANTS HELP CLIENTS</h1>
                <div class="btn-prev-next">
                    <button>
                        <img src="/public/images/prev.png" alt="">
                    </button>
                    <button>
                        <img src="/public/images/next.png" alt="">
                    </button>
                </div>
            </div>
            <div class="row d-flex gap-1">
                <div class="col-4 posi-rela" v-for="img in images">
                    <img :src="'/public/images/' + img" alt="">
                    <div class="overlay d-flex">
                        <div class="info-product d-flex">
                            <div class="info">
                                <h3>Purinky Products</h3>
                                <span>uncatogorized</span>
                            </div>
                            <div class="plus">
                                <i class="fa-solid fa-plus"></i>
                            </div>
                        </div>

                    </div>
                </div>
            </div>

        </div>
    </section>
</template>

<style></style>