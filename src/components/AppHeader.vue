<script>
export default {
    data() {
        return {

        }
    }
}
</script>

<template>
    <header>
        <div class="logo">
            <img src="../assets/img/dc-logo.png" alt="header-logo">
        </div>
        <ul>
            <li><a href="">CHARACTERS</a></li>
            <li><a href="">COMICS</a></li>
            <li><a href="">MOVIES</a></li>
            <li><a href="">TV</a></li>
            <li><a href="">GAMES</a></li>
            <li><a href="">COLLECTIBLES</a></li>
            <li><a href="">VIDEOS</a></li>
            <li><a href="">FANS</a></li>
            <li><a href="">NEWS</a></li>
            <li><a href="">SHOP</a></li>
        </ul>
    </header>
</template>

<style scoped lang="scss">
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

header {
    height: 16vh;
    @include flex (row, space-between, center)
}

ul {
    @include flex(row, space-between, center);
    list-style-type: none;
    gap: 1rem;
    margin-right: 80px;
    font-size: 0.9rem;

    a {
        text-decoration: none;
        color: $header-text-color;

        &:hover {
            color: $primary-color;
        }
    }
}

.logo {
    margin-left: 150px;

    img {
        width: 60px;
    }
}
</style>