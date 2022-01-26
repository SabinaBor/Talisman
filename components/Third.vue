<template>
<div id="third" class="main__right__third full-height">
    <p><span class="title">Галерея</span></p>
    <p><span class="title"><strong>TALISMAN</strong> RESIDENTIAL COMPLEX</span></p>
    <div class="main__right__gallery">
        <div v-for="i in 8" :key="i + 'c'" class="main__right__gallery__item">
            <vue-flip active-hover :height="'100%'" :width="'100%'" transition="1s">
                <template v-slot:front>
                    <div class="main__right__gallery__image">
                    </div>
                </template>
                <template v-slot:back>
                    <div class="main__right__gallery__text">
                        HELLO, THIS IS BACKYARD
                    </div>
                </template>
            </vue-flip>
        </div>
    </div>
</div>
</template>

<script>
import VueFlip from 'vue-flip';

export default {
    name: "ThirdComponent",
    components: {
        'vue-flip': VueFlip
    }
}
</script>

<style lang="scss">
.main__right__third {
    p {
        margin-bottom: 2.4vw;
        &:first-child {
            margin-bottom: 0;
        }
        span.title {
            margin-bottom: 0;
        }
    }
    .main__right__gallery {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-template-rows: repeat(2, 16.5vw);
        width: 100%;
        &__item {
            .main__right__gallery__image {
                width: 100%;
                height: 100%;
            }
            .main__right__gallery__text {
                text-align: center;
                width: 100%;
                height: 100%;
            }
            &:nth-child(1) {
                .main__right__gallery__image {
                    background: url("/six.png") no-repeat center bottom;
                    background-size: cover;
                }
            }
            &:nth-child(2) {
                .main__right__gallery__image {
                    background: url("/third.png") no-repeat center center;
                    background-size: cover;
                }
            }
            &:nth-child(3) {
                .main__right__gallery__image {
                    background: url("/seventh.png") no-repeat center bottom;
                    background-size: cover;
                }
            }
            &:nth-child(4) {
                .main__right__gallery__image {
                    background: url("/eight.png") no-repeat center center;
                    background-size: cover;
                }
            }
            &:nth-child(5) {
                .main__right__gallery__image {
                    background: url("/11.png") no-repeat center bottom;
                    background-size: cover;
                }
            }
            &:nth-child(6) {
                .main__right__gallery__image {
                    background: url("/10.png") no-repeat center bottom;
                    background-size: cover;
                }
            }
            &:nth-child(7) {
                .main__right__gallery__image {
                    background: url("/12.png") no-repeat center bottom;
                    background-size: cover;
                }
            }
            &:nth-child(8) {
                .main__right__gallery__image {
                    background: url("/nine.png") no-repeat center center;
                    background-size: cover;
                }
            }
            &:hover {
                cursor: pointer;
            }
        }
    }
}
.flip-container {
    .front, .back {
        width: 100%;
        height: 100%;
    }
}
</style>
