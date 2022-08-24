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

    &.shadow {
        box-shadow: 0px 0px 10px 1px #AEAEAE;
    }

    &.regular {
        background-color: $primary;


        &:hover {
            color: #fff;
            background-color: $success;
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