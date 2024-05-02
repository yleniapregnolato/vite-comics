<script>
import AppSectionMain from './AppSectionMain.vue';

export default {
    data() {
        return {};
    },
    components: { AppSectionMain }
}
</script>

<template>
    <main>
        <!-- hero section -->
        <section class="hero">
            <h2> --> Content Goes here <-- </h2>
        </section>

        <!-- merchandising-section -->
        <AppSectionMain />

        <!--  -->
    </main>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

.hero {
    height: 16vh;
    background-color: $main-background-color;
    color: white;
    font-size: 0.8rem;
    
    h2 {
        padding-left: 150px;
        padding-top: 40px;
    }
}

</style>