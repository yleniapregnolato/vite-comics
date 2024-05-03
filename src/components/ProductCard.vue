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
        height: 100px;
        width: 100px;
        object-fit: cover;      
    }

    h4 {
        font-weight: 300;
        padding-top: 10px;
    }
    padding-top: 20px;
    margin-bottom: 20px;
}
</style>