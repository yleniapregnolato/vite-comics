<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <footer>
        <!-- first section -->
        <section class="info-dc"></section>
        <!-- /first section -->

        <!-- second section -->
        <section class="icons"></section>
        <!-- /second section -->
    </footer>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

footer {
    height: 52vh;

    .info-dc {
        height: 45vh;
        background-image: url(../assets/img/footer-bg.jpg);
        background-size: cover;
    }


    .icons {
        height: 10vh;
        background-color: $footer-background-color;
    }
}
</style>