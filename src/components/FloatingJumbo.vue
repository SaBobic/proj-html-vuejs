<template>
    <div>
        <div v-for="item in items" :key="item.id" :class="['row', { 'flex-row-reverse': item.direction === false }]">
            <div class="col-6">
                <img :src="require(`../assets/img/${item.icon}`)" alt="" class="floating-jumbo-icon">
                <h3 class="floating-jumbo-title">{{ item.title }}</h3>
                <p class="floating-jumbo-text">{{ item.text }}</p>
                <MainButton :anchor="item.anchor" :url="item.url" scheme="regular danger" />
            </div>
            <div class="col-6 text-center align-items-center">
                <img class="floating-jumbo-img" :src="require(`../assets/img/${item.img}`)" alt="">
            </div>
        </div>
    </div>
</template>

<script>
import MainButton from './MainButton.vue';
export default {
    name: "FloatingJumbo",
    props: {
        items: Array,
    },
    components: { MainButton }
}
</script>

<style lang="scss" scoped>
.row {
    margin-bottom: 100px;

    &:last-of-type {
        margin-bottom: 0;
    }
}

.floating-jumbo-icon {
    height: 60px;
    margin-bottom: 20px;
}

.floating-jumbo-title {
    margin-bottom: 30px;
}

.floating-jumbo-text {
    margin-bottom: 40px;
    max-width: 420px;
}

.floating-jumbo-img {
    padding-top: 50px;
    max-width: 500px;
}
</style>