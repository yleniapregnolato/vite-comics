<script>
export default {
    data() {
        return {
            image: [
                {
                    image: "buy-comics-digital-comics.png",
                    title: "DIGITAL COMICS"
                },
                {
                    image: "buy-comics-merchandise.png",
                    title: "DC MERCHANDISE"
                },
                {
                    image: "buy-comics-shop-locator.png",
                    title: "SUBSCRIPTION"
                },
                {
                    image: "buy-comics-subscriptions.png",
                    title: "COMIC SHOP LOCATOR"
                },
                {
                    image: "buy-dc-power-visa.svg",
                    title: "DC POWER VISA"
                }
            ]

        }
    },
    methods: {
        getImageUrl(imageName) {
            return new URL(`../assets/img/${imageName}`, import.meta.url).href;
        },
    },
};
</script>

<template>
    <div class="container">
        <div class="row">
            <ul v-for="item in image">
                <li><img :src="getImageUrl(item.image)" alt=""></li>
                <h4>{{ item.title }}</h4>
            </ul>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.container {
    @include flex(row, space-between, center, nowrap);
    background-color: $primary-color;

    .row {
        @include flex(row, space-between, center, nowrap);
        width: 70%;
        margin: 0 auto;
    }

    ul {
        @include flex(row, space-between, center, nowrap);
        gap: 5px;
        list-style-type: none;
        padding-top: 20px;
        padding-bottom: 20px;

        h4 {
            color: white;
            font-weight: 400;
            font-size: 0.8rem;
        }
    }

    img {
        height: 35px;
    }
}</style>