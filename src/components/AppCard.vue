<script>
export default {
    props: {
        thumb: String,
        series: String
    }
}
</script>

<template>
    <div class="card">
        <img :src="thumb" alt="">
        <h3>{{ series }}</h3>
    </div>
</template>

<style lang="scss" scoped>
.card {
    height: 100%;

    img {
        height: 170px;
        width: 170px;
    }
}
</style>