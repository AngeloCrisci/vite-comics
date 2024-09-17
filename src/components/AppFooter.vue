<script>
export default {
    data() {
        return {
            name: 'AppFooter',
            footerList: [
                { title: 'DC Comics', subtitle: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News'] },
                { title: 'Shop', subtitle: ['Shop DC', 'Shop DC Collectibles'] },
                { title: 'DC', subtitle: ['Term of use', 'Privacy policy(New)', 'AD choice', 'Advertising', 'Jobs', 'Subscription', 'Talent Workshop', 'CPSC Certificate', 'Ratings', 'Shop Help', 'Contact us'] },
                { title: 'Sites', subtitle: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa'] },
            ]
        }
    }
}
</script>

<template>
    <footer>
        <section id="top-footer">
            <div class="container d-flex">
                <div class="link-list col-md-8">
                    <div class="row">
                        <div v-for="(item, index) in footerList" :key="index" class="col">
                            <h5>
                                {{ item.title }}
                            </h5>
                            <ul>
                                <li v-for="( subitem, i) in item.subtitle" :key="i">
                                    <a href="#"> {{ subitem }} </a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="col-md-4 logo">
                    <img src="../assets/img/dc-logo-bg.png" alt="Logo Big">
                </div>
            </div>
        </section>
        <section id="bottom-footer">
            <div class="footer-jumbotron container d-flex align-items-center justify-content-between">
                <div class="sign-up col-7">
                    <button type="button" class="btn btn-outline-primary">SIGN-UP NOW!</button>
                </div>
                <div class="icons-footer d-flex col-5 gap-5">
                    <a href="#">
                        FOLLOW US
                    </a>
                    <img src="../assets/img/footer-periscope.png" alt="">
                    <img src="../assets/img/footer-pinterest.png" alt="">
                    <img src="../assets/img/footer-twitter.png" alt="">
                    <img src="../assets/img/footer-youtube.png" alt="">
                    <img src="../assets/img/footer-facebook.png" alt="">
                </div>
            </div>
        </section>
    </footer>
</template>

<style scoped lang="scss">
#top-footer {
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    padding: 20px 0;
}

.logo {
    img {}
}

li {
    list-style-type: none;
    margin-left: 0;

    a {
        text-decoration: none;
        color: #787878;
    }
}

h5 {
    color: gainsboro;
}

ul {
    padding-left: 0;
}

#bottom-footer {
    height: 150px;
    background-color: #2C2C2C;
}


.icons-footer {
    a {
        text-decoration: none;
    }
}

.footer-jumbotron {
    height: 100%;
}
</style>