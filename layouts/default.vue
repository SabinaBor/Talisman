<template>
    <div class="main">
        <div class="main__left">
            <Logo />
            <div class="main__menu">
                <div class="main__menu__dot"></div>
                <div class="main__menu__dot"></div>
                <div class="main__menu__dot"></div>
                <div class="main__menu__dot"></div>
                <div class="main__menu__dot"></div>
                <div class="main__menu__dot"></div>
                <div class="main__menu__dot"></div>
                <div class="main__menu__dot"></div>
                <div class="main__menu__dot"></div>
            </div>
        </div>
        <div class="main__right">
            <Nuxt />
        </div>
    </div>
</template>

<script>
import Logo from "@/components/svg/Logo";

export default {
    name: "DefaultLayout",
    components: {
        Logo
    },
    mounted() {
        window.addEventListener("scroll", this.scrollHandle);
    },
    computed: {
        windowHeight() {
            return window.innerHeight;
        }
    },
    methods: {
        scrollHandle () {
            console.log(window.scrollY)        
        },
    }
}
</script>

<style lang="scss">
.main {
    height: 100vh;
    overflow-y: auto;
    &__left {
        background: #fff;
        padding: 40px 20px;
        display: flex;
        flex-direction: column;
        position: fixed;
        width: 100px;
        height: 100vh;
        top: 0;
        left: 0;
    }
    &__right {
        margin-left: 100px;
    }
    &__menu {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-top: 100px;
        &__dot {
            border: 2px solid #A3A3A3;
            border-radius: 50%;
            width: 10px;
            height: 10px;
            margin-bottom: 14px;
            &:hover {
                cursor: pointer;
            }
        }
    }
}
</style>