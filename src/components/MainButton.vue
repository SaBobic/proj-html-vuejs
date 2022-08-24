<template>
    <a :class="['main-btn', scheme]" :href="url">{{ anchor }}</a>
</template>

<script>
export default {
    name: 'MainButton',
    props: {
        anchor: String,
        scheme: String,
        url: String,
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars';

.main-btn {
    display: inline-block;
    font-family: 'Fredoka One', cursive;
    font-size: 14px;
    padding: 23px 45px;
    border-radius: 35px;

    &.regular {
        background-color: $primary;


        &.success:hover {
            color: #fff;
            background-color: $success;
        }

        &.shadow:hover {
            color: #fff;
            background-color: $danger;
            box-shadow: 0 0 20px rgba($color: #000000, $alpha: 0.2);
        }
    }

    &.danger {
        background-color: $danger;

        &:hover {
            color: #fff;
            background-color: $primary;
        }

    }
}
</style>