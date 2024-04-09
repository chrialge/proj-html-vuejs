<script>
export default {
    name: 'OurConsultation',
    data() {
        return {
            dataConsulting: [
                { icon: '<i class="fa-solid fa-chart-line"></i>', title: 'STATIC CONSULTING' },
                { icon: '<i class="fa-solid fa-bullhorn"></i>', title: 'DIGITAL CONSULTING' },
                { icon: '<i class="fa-solid fa-wallet"></i>', title: 'BANKING CONSULTING' },
                { icon: '<i class="fa-solid fa-bullseye"></i>', title: 'ENTERPRISE CONSULTING' },

            ]
        }
    }
}
</script>

<template>

    <section id="our-consultation">
        <div class="container-sm">
            <div class="title d-flex">
                <h1>OUR CONSULTANTS CAN HELP YOU</h1>
                <div class="separeted_small width-long posi-abso"></div>
            </div>
            <div class="row d-flex">
                <div class="col-6-50 d-flex" v-for="consulting in dataConsulting">
                    <div class="icon" v-html="consulting.icon">
                    </div>
                    <div class="info">
                        <h4>{{ consulting.title }}</h4>
                        <p class="paragraph">
                            When, while lovely valley teems with vapour around meand eridian sun strikes the upper
                            impernetraable foliage of my trees, and but a
                        </p>
                    </div>
                </div>
            </div>
        </div>

    </section>
</template>



<style></style>