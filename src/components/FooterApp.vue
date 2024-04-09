<script>
export default {
    name: 'FooterApp',
    data() {
        return {
            msg: 'footer',
            navbar: [
                { name: 'HOME', href: '#jumbotron' },
                { name: 'ABOUT', href: '#about-us' },
                { name: 'PROJECTS', href: '#projects' },
                { name: 'SERVICES', href: '#testimonials' },
                { name: 'BLOG', href: '#blog' },
                { name: 'CONTACT', href: '#site-footer' }
            ],
            icons: [
                '<i class="fa-brands fa-instagram"></i>',
                '<i class="fa-brands fa-linkedin-in"></i>',
                '<i class="fa-brands fa-facebook-f"></i>',
                '<i class="fa-brands fa-twitter"></i>'
            ]
        }
    }
}
</script>

<template>
    <footer id="site_footer">
        <div class="container">
            <div class="footer_top d-flex">
                <div class="logo">
                    <img src="/public/images/logotype-2-150x25.png" alt="">
                </div>
                <div class="navbar">
                    <ul class="d-flex gap-1">
                        <li v-for="section in navbar">
                            <a :href="section.href">
                                {{ section.name }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="social">
                    <ul class="d-flex gap-1">
                        <li v-for="icon in icons"><a href="#" v-html="icon"></a></li>
                    </ul>
                </div>
            </div>
            <div class="separeted-footer"></div>
            <div class="footer-bottom d-flex">
                <div class="policy">
                    <ul>
                        <li><a href="#">Terms of use</a></li>
                        <li><a href="#">Privacy Environmental</a></li>
                    </ul>
                </div>
                <div class="copyright">
                    Copyright &copy; 2020 Phlox Consulting.All Rights Reserved.
                </div>
            </div>
        </div>

    </footer>
</template>

<style></style>
