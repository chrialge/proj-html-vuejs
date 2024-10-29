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
            ]
        }
    },
    methods: {

        /**
         * funzione che manda indietrole immagini dello slider del testimonial
         */
        prev() {

            // salvo la lunghezza della finestra
            const widthDevice = window.innerWidth;

            // salvo le card 
            const boxImageEl = document.querySelectorAll(".box-image");

            // se la lunghezza della finestra e minore di 900
            if (widthDevice <= 900) {

                // se activeImageMobile e uguale a 0
                if (this.activeImageMobile === 0) {

                    // activeImageMobile e uguale alla lunghezza di image meno 1
                    this.activeImageMobile = this.images.length - 1


                    // itero nelle immagini
                    this.images.forEach((img, index) => {

                        // se l'index e uguale ad activeImageMobile
                        if (index === this.activeImageMobile) {

                            // cambio l'attributo src dell'immagine
                            boxImageEl[0].setAttribute('src', `./images/${img.img}`)
                        }
                    })


                } else {

                    // decremento activeImageMobile
                    this.activeImageMobile--

                    // itero nelle immagini
                    this.images.forEach((img, index) => {

                        // se l'index e uguale activeImageMobile
                        if (index === this.activeImageMobile) {

                            // cambio l'attributo src dell'immagine
                            boxImageEl[0].setAttribute('src', `./images/${img.img}`)
                        }
                    })
                }
            } else {

                // salvo i numeri mappati
                const numberImage = this.activeImage.map((number) => {

                    // se il numro e 0
                    if (number === 0) {

                        // return della lunghezza di images meno 1
                        return this.images.length - 1
                    } else {

                        // return del numero decrementato
                        return number - 1
                    }

                })

                // sovrascrivo l'istanza activeImage con numberImage
                this.activeImage = numberImage

                // inizializzo un contattore
                let count = 0

                // itero in activeImage
                this.activeImage.forEach((imagenew) => {

                    // itero nelle immagine
                    this.images.forEach((img, index) => {

                        // se l'index e uguale a imagenew
                        if (index === imagenew) {

                            // cambio l'attributo src delle immmagini
                            boxImageEl[count].setAttribute('src', `./images/${img.img}`)

                            //incremento contatore
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

            // salvo la lunghezza della finestra
            const widthDevice = window.innerWidth;

            // salvo le card 
            const boxImageEl = document.querySelectorAll(".box-image");

            // se la lunghezza e superiore a 900 pixel
            if (widthDevice <= 900) {

                // se activeImageMobile e uguale alla lunghezza di images meno uno
                if (this.activeImageMobile === (this.images.length - 1)) {

                    // activeImageMobilr diventa 0
                    this.activeImageMobile = 0

                    // itero in images
                    this.images.forEach((img, index) => {

                        // se l'index di images e uguale a activeImageMobile
                        if (index === this.activeImageMobile) {

                            // cambio attributto di src
                            boxImageEl[0].setAttribute('src', `./images/${img.img}`)
                        }
                    })


                } else {

                    // incremento di 1 activeImageMobile
                    this.activeImageMobile++

                    // itero in images
                    this.images.forEach((img, index) => {

                        // se l'index di images e uguale a activeImageMobile
                        if (index === this.activeImageMobile) {

                            // cambio attributto di src
                            boxImageEl[0].setAttribute('src', `./images/${img.img}`)
                        }
                    })



                }
            } else {

                // salvo i numeri mappati
                const numberImage = this.activeImage.map((number) => {

                    // se il numero e uguale alla lunghezza di images meno 1
                    if (number === (this.images.length - 1)) {

                        // ritorna 0
                        return 0
                    } else {

                        // ritorna il numero incrementato di 1
                        return number + 1
                    }

                })

                // sovrascrivo l'istanta con numerImage
                this.activeImage = numberImage

                // inizializzo un contattore
                let count = 0

                // itero in activeImage
                this.activeImage.forEach((imagenew) => {

                    // itero tra le immagini
                    this.images.forEach((img, index) => {

                        // se l'index e uguale ad imagenew
                        if (index === imagenew) {

                            // cambio lattributo dell'src
                            boxImageEl[count].setAttribute('src', `./images/${img.img}`)

                            // incremento il contatore
                            count++

                        }
                    })
                })



            }

        },

    },
    mounted() {
        // salvo il nodo dove inseriro le card
        const containerCard = document.querySelector('#project>.container>.row');


        // salvo la lunghezza della finestra
        const widthDevice = window.innerWidth;

        // se la finestra e minore di 900 pixel
        if (widthDevice < 900) {

            // ciclo tra le immagini
            this.images.forEach((img, index) => {

                // se l'index delle immagini e uguale all'istanza activeImageMobile
                if (index === this.activeImageMobile) {

                    // costante dove contengo il markup e cambia l'immagine in base all'index
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
                    // aggiungo al containeril markup
                    containerCard.insertAdjacentHTML('beforeend', markup)
                }
            })

        } else {

            // ciclo nell'array delle immagini attive
            this.activeImage.forEach((imageActive) => {

                // ciclo tra le immagine
                this.images.forEach((img, index) => {

                    // se l'immagine attiva e uguale all index
                    if (imageActive === index) {

                        // costante dove contengo il markup e cambia l'immagine in base all'index
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
                        // aggiungo al containeril markup
                        containerCard.insertAdjacentHTML('beforeend', markup)
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