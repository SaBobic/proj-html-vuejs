<template>
    <section id="main-newsletter">
        <div class="container">
            <div class="row">
                <div class="col-7 newsletter-text">Subscribe Now to Our Newsletter!</div>
                <div class="col-5 newsletter-input">
                    <input type="text" placeholder="Email address...">
                    <div class="submit-button c-pointer"></div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'MainNewsletter',
}
</script>

<style lang="scss" scoped>
@import '../assets/scss/vars';

#main-newsletter {
    padding: 70px 0;
    background-color: $danger;

    .newsletter-text {
        font-size: 35px;
        line-height: 70px;
        vertical-align: middle;
        color: #fff;
        font-family: 'Fredoka One', cursive;
    }

    .newsletter-input {
        position: relative;

        input {
            width: 100%;
            height: 70px;
            border: 0;
            border-radius: 50px;
            padding-left: 30px;

            &:focus-visible {
                outline: 0;
            }
        }

        .submit-button {
            background-color: $primary;
            height: 70px;
            width: 70px;
            border-radius: 50%;
            color: #fff;
            position: absolute;
            right: 0;
            top: 50%;
            transform: translateY(-50%);

            &::before {
                font: var(--fa-font-solid);
                content: '\f1d8';
                font-size: 20px;
                position: absolute;
                top: 50%;
                left: 50%;
                transform: translate(-50%, -50%);
            }

            &:hover {
                background-color: $danger;
                box-shadow: 0 0 20px rgba($color: #000000, $alpha: 0.2);
            }
        }
    }
}
</style>