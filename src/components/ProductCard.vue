<script>
export default {
    props: {
        cardImage: String,
        cardTitle: String,
    }
}
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
            max-width: 100%;
            aspect-ratio: 1;
            object-fit: cover;
            object-position: left top;
        }

        h4 {
            font-size: 0.7rem;
            color: rgb(170, 170, 170);
        }
    }
</style>