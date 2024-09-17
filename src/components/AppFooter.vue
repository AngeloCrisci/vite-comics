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
    img {
        position: relative;
        z-index: 0;
    }
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
    position: relative;
    bottom: 0;
    z-index: 2;
    height: 100px;
    background-color: #2C2C2C;
}
</style>