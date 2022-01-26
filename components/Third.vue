<template>
<div id="third" class="main__right__third full-height">
    <p><span class="title">Галерея</span></p>
    <p><span class="title"><strong>TALISMAN</strong> RESIDENTIAL COMPLEX</span></p>
    <div class="main__right__gallery">
        <div @click="showGallery(id)" v-for="(img, id) in galleryList" :key="id + 'c'" class="main__right__gallery__item">
            <vue-flip active-hover :height="'100%'" :width="'100%'" transition="1s">
                <template v-slot:front>
                    <div class="main__right__gallery__image">
                        <img :src="img.url" />
                    </div>
                </template>
                <template v-slot:back>
                    <div class="main__right__gallery__text">
                        <div class="main__right__gallery__number">
                            {{ id + 1 }}
                        </div>
                        <p>{{img.name}}</p>
                        <p>TALISMAN RESIDENTIAL<br />COMPLEX</p>
                    </div>
                </template>
            </vue-flip>
        </div>
    </div>
    <div v-if="isModalOpened" class="modal">
        <div @click="isModalOpened = false" class="empty"></div>
        <div class='container'>
      <client-only>
        <slider
          v-model='sliderIndex'
          animation="fade"
          stop-on-hover
          :interval='6000'
        >
            <slider-item v-for="(image, index) in galleryList" :key="index">
              <div class="img__wrapper">
                <img :src="image.url" />
              </div>
            </slider-item>
        </slider>
      </client-only>
    </div>
    </div>
</div>
</template>

<script>
import VueFlip from 'vue-flip';
import {Slider, SliderItem} from 'vue-easy-slider'

export default {
    name: "ThirdComponent",
    components: {
        'vue-flip': VueFlip,
        Slider,
        SliderItem
    },
    data() {
        return {
            isModalOpened: false,
            sliderIndex: 0,
            galleryList: [
                {
                    id: 1,
                    name: "Беседка в зоне отдыха",
                    url: "/six.png"
                },
                {
                    id: 2,
                    name: "Перед одного из домов",
                    url: "/third.png"
                },
                {
                    id: 3,
                    name: "Внутренний двор",
                    url: "/seventh.png"
                },
                {
                    id: 4,
                    name: "Кафе",
                    url: "/eight.png"
                },
                {
                    id: 5,
                    name: "Парковка ",
                    url: "/11.png"
                },
                {
                    id: 6,
                    name: "Подземная парковка",
                    url: "/10.png"
                },
                {
                    id: 7,
                    name: "Парковка",
                    url: "/12.png"
                },
                {
                    id: 8,
                    name: "Магазины у",
                    url: "/nine.png"
                }
            ]
        }
    },
    methods: {
        showGallery(id) {
            this.isModalOpened = true;
            this.sliderIndex = id;
        }
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
                img {
                    width: 100%;
                    height: 100%;
                }
            }
            .main__right__gallery__text {
                text-align: center;
                width: 100%;
                height: 100%;
            }
            &:hover {
                cursor: pointer;
            }
        }
        &__text {
            background: #A3A3A3;
            padding: 45px 42px 70px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            p {
                font-size : 0.8vw;
                letter-spacing : 0.35px;
                color : #fff;
                font-family: "FiraSans-Semibold";
                margin-bottom: 0;
                &:last-child {
                    font-family: "FiraSans-Regular";
                }
            }
        }
        &__number {
            width: 85px;
            height: 85px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 4vw;
            border: 5px solid #fff;
            color: #fff;
            margin-bottom: 40px;
        }
    }
}
.flip-container {
    .front, .back {
        width: 100%;
        height: 100%;
    }
}

  .modal {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 10000;
    display: flex;
    justify-content: center;
    align-items: center;
    .empty {
        width: 100%;
        height: 100%;
        opacity : 0.75;
        background: #000;
        position: absolute;
        top: 0;
        left: 0;
    }
    .container {
        width: 70%;
        height: 70%;
        max-width: 70%;
        display: flex;
        justify-content: center;
        align-items: center;
        .slider {
            width: 100%!important;
            height: 100%!important;
            img {
                width: 100%;
            }
        }
    }
  }
</style>
