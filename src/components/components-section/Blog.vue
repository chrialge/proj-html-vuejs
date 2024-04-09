<script>
export default {
    name: 'Blog',
    data() {
        return {
            images: [
                'startup-business-people-and-strategy-board-PAJ3P9K-1390x1042.jpg',
                'business-people-working-together-on-project-and-5FHSKBL-1390.jpg'
            ]
        }
    }
}
</script>

<template>
    <section id="blog">
        <div class="container">
            <div class="section">
                <div class="separeted_small"></div>
                <span>BLOG</span>
            </div>
            <div class="header-blog d-flex">
                <h1>THE RECENT NEWS YOU MUST READ IT</h1>
                <button class="btn">view all</button>
            </div>
            <div class="row d-flex gap-1">
                <div class="img col-2" v-for="img in images">
                    <img :src="'../../../public/images/' + img " 
                        alt="startup business people and strategy board">
                    <div class="banner-img">
                        <div class="info_banner_img">
                            <span>July 4,2019</span>
                            <span>by paul</span>
                        </div>
                        <h3>
                            Canadian Consulting Firm acquired by UK Giant
                        </h3>
                        <p class="paragraph">
                            When, while lovely valley teems with vapour around meand eridian sun strikes the upper
                            impernetraable foliage of my trees, and but a ...
                        </p>
                    </div>
                </div>
            </div>


        </div>
    </section>
</template>

<style></style>