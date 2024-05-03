<script>
export default {
    data() {
        return {
            dcComics: ["Characters", "Comics, Movies", "TV", "Games", "Videos", "News"],
            shop: ["Shop DC", "Shop DC Collectibles"],
            dc: ["Terms Of Use", "Privacy policy (New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"],
            sites: ["DC", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"],
        };
    }
}
</script>

<template>
    <footer>
        <!-- first section -->
        <section class="info-dc">

            <div class="container">
                <div class="col">
                    <h2>DC COMICS</h2>
                    <ul class="comics" v-for="comics in dcComics">

                        <li><a href="">{{ comics }}</a></li>
                    </ul>

                    <h2>SHOP</h2>
                    <ul class="shop" v-for="items in shop">
                        <li><a href="">{{ items }}</a></li>
                    </ul>
                </div>

                <div class="col">
                    <h2>DC</h2>
                    <ul class="dc" v-for="info in dc">
                        <li><a href="">{{ info }}</a></li>
                    </ul>
                </div>
                <div class="col">
                    <h2>SITES</h2>
                    <ul class="sites" v-for="site in sites">
                        <li><a href="">{{ site }}</a></li>
                    </ul>
                </div>


            </div>
            <!-- /first section -->

            <!-- second section -->
            <section class="icons"></section>
            <!-- /second section -->
        </section>

    </footer>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

footer {
    .info-dc {
        background-image: url(../assets/img/dc-logo-bg.png), url(../assets/img/footer-bg.jpg);
        background-size: 40%, cover;
        background-repeat: no-repeat;
        background-position: right 90px top -60px, center;
    }

    .container {
        @include flex(row, flex-start, flex-start, wrap);
        width: 60%;
        margin-left: 100px;

        .col {
            @include flex(column, flex-start, flex-start, nowrap);
            width: calc(100% / 3);
            gap: 10px;
            padding-top: 30px;
            padding-bottom: 30px;

            h2 {
                color: white;
            }

            li {
                list-style-type: none;

                a {
                    text-decoration: none;
                    color: $text-footer;
                }
            }
        }


    }


    .icons {
        height: 10vh;
        background-color: $footer-background-color;
    }
}
</style>