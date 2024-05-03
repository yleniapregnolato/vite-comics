<script>

export default {
    props: {
        cardImage: String,
        cardTitle: String,
    },

};
</script>

<template>
    <div class="card">
        <img :src="cardImage" :alt="cardTitle">
        <h4>{{ cardTitle }}</h4>
    </div>
</template>

<style scoped lang="scss">
.card {
    img {
        width: 60%;
    }

    padding-top: 20px;
    margin-bottom: 20px;
}
</style>