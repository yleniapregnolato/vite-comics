<script>
import AppSectionMain from './AppSectionMain.vue';
import { productsArray } from "../assets/data/products";
import ProductCard from './ProductCard.vue';

export default {
    data() {
        return {
            products: productsArray
        };
    },
    components: { AppSectionMain, ProductCard }
}
</script>

<template>
    <main>
        <!-- products section -->
        <section class="hero">
            <div class="hero-container">
            </div>
            <div class="container">
                <div class="row">
                    <div class="col" v-for="prod in products">
                        <ProductCard :cardImage="prod.thumb" :cardTitle="prod.series" />
                    </div>
                </div>

            </div>

        </section>

        <!-- /products section -->

        <!-- merchandising-section -->
        <AppSectionMain />

    </main>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.hero-container {
    background-image: url(../assets/img/jumbotron.jpg);
    height: 50vh;
    background-size: cover;
}

.hero {
    background-color: $main-background-color;
    color: white;
    font-size: 0.8rem;

    h2 {
        padding-left: 150px;
        padding-top: 40px;
    }
}

.container {
    width: 70%;
    margin: 0 auto;

    .row {
       @include flex(row, space-between, stretch, wrap); 

       .col {
        width: 15%;
       }
    }
}
</style>