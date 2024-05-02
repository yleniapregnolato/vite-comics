<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <main>
        <h2> --> Content Goes here <-- </h2>
    </main>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

main {
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