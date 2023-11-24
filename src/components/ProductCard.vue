<script>
export default {
    props: {
        title: String,
        image: String,
    }
}
</script>

<template>
    <div class="card">
        <img :src="image" alt="" />
        <h3>{{ title }}</h3>
    </div>
</template>

<style scoped lang="scss">
.card {
    background-color: #1c1c1c;
    height: 100%;

    img {
        height: 200px;
        width: 200px;
    }

    h3 {
        color: white;
    }
}
</style>