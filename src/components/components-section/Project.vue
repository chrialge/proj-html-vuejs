<script>
export default {
    name: 'Project',
    data() {
        return {
            activeImage: [0, 1, 2],
            activeImageMobile: 0,
            images: [
                { id: 0, img: 'DRY-1-790x592.jpg' },
                { id: 1, img: '221bf0b7-8134-43bb-936a-5acbe42db64a-790x592.jpg' },
                { id: 2, img: 'z1el4c4p-790x592.jpg' },
                { id: 3, img: 'oliver-ragfelt-488196-2.jpg' },
                { id: 4, img: 'oliver-ragfelt-488196-unsplash.jpg' },
            ]
        }
    },
    methods: {

        /**
         * funzione che manda indietrole immagini dello slider del testimonial
         */
        prev() {
            const widthDevice = window.innerWidth;

            const containerCrad = document.querySelector('#project>.container>.row');
            const boxImageEl = document.querySelectorAll(".box-image");

            if (widthDevice <= 900) {


                if (this.activeImageMobile === 0) {
                    this.activeImage = this.images.length - 1

                    this.images.forEach((img, index) => {
                        if (index === this.activeImageMobile) {

                            boxImageEl[0].setAttribute('src', `./images/${img.img}`)
                        }
                    })


                } else {
                    this.activeImageMobile--


                    this.images.forEach((img, index) => {
                        if (index === this.activeImageMobile) {

                            boxImageEl[0].setAttribute('src', `./images/${img.img}`)
                        }
                    })



                }
            } else {
                console.log(document.querySelectorAll(".box-image"));





                const numberImage = this.activeImage.map((number) => {
                    if (number === (this.images.length - 1)) {
                        return 4
                    } else {
                        return number - 1
                    }

                })
                this.activeImage = numberImage

                console.log(this.activeImage, numberImage);

                let count = 0

                this.activeImage.forEach((imagenew) => {


                    this.images.forEach((img, index) => {
                        if (index === imagenew) {
                            boxImageEl[count].setAttribute('src', `./images/${img.img}`)
                            count++

                        }
                    })
                })



            }
        },

        /**
        * funzione che manda avanti le immagini dello slider del testimonial
        */
        next() {
            const widthDevice = window.innerWidth;

            const containerCrad = document.querySelector('#project>.container>.row');
            const boxImageEl = document.querySelectorAll(".box-image");

            if (widthDevice <= 900) {
                console.log(this.activeImageMobile)


                if (this.activeImageMobile === (this.images.length - 1)) {
                    this.activeImageMobile = 0

                    this.images.forEach((img, index) => {
                        if (index === this.activeImageMobile) {

                            boxImageEl[0].setAttribute('src', `./images/${img.img}`)
                        }
                    })


                } else {
                    this.activeImageMobile++


                    this.images.forEach((img, index) => {
                        if (index === this.activeImageMobile) {

                            boxImageEl[0].setAttribute('src', `./images/${img.img}`)
                        }
                    })



                }
            } else {
                console.log(document.querySelectorAll(".box-image"));





                const numberImage = this.activeImage.map((number) => {
                    if (number === 4) {
                        return 0
                    } else {
                        return number + 1
                    }

                })
                this.activeImage = numberImage

                console.log(this.activeImage, numberImage);

                let count = 0

                this.activeImage.forEach((imagenew) => {


                    this.images.forEach((img, index) => {
                        if (index === imagenew) {
                            boxImageEl[count].setAttribute('src', `./images/${img.img}`)
                            count++

                        }
                    })
                })



            }

        },

    },
    mounted() {
        const containerCrad = document.querySelector('#project>.container>.row');



        const widthDevice = window.innerWidth;
        // const cardEl = document.querySelectorAll('.card-project');

        if (widthDevice < 900) {


            this.images.forEach((img, index) => {
                if (index === this.activeImageMobile) {

                    const markup = `
                        <div class="col-4 posi-rela card-project" >
                    <img src="./images/${img.img}" alt="" class="box-image">
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
                    `
                    containerCrad.insertAdjacentHTML('beforeend', markup)
                }
            })

        } else {

            this.activeImage.forEach((imageActive) => {
                // console.log(imageActive)

                this.images.forEach((img, index) => {
                    if (imageActive === index) {

                        const markup = `
                        <div class="col-4 posi-rela card-project" >
                    <img src="./images/${img.img}" alt="" class="box-image">
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
                    `
                        containerCrad.insertAdjacentHTML('beforeend', markup)
                    }
                })
            })



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
                    <button @click="prev()">
                        <img src="/images/prev.png" alt="">
                    </button>
                    <button @click="next()">
                        <img src="/images/next.png" alt="">
                    </button>
                </div>
            </div>
            <div class="row d-flex gap-1">

            </div>

        </div>
    </section>
</template>

<style></style>