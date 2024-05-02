<script>
export default {
    data() {
        return {
            menu: [
                {
                    title: "CHARACTERS",
                    isActive: false
                },
                {
                    title: "COMICS",
                    isActive: false
                },
                {
                    title: "MOVIES",
                    isActive: false
                },
                {
                    title: "TV",
                    isActive: false
                },
                {
                    title: "GAMES",
                    isActive: false
                },
                {
                    title: "COLLECTIBLES",
                    isActive: false
                },
                {
                    title: "VIDEOS",
                    isActive: false
                },
                {
                    title: "FANS",
                    isActive: false
                },
                {
                    title: "NEWS",
                    isActive: false
                },
                {
                    title: "SHOP",
                    isActive: false
                },
            ]

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
            <li v-for="item in menu">
                <a href="" :class="{ active: item.isActive }">{{ item.title }}</a>
            </li>
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