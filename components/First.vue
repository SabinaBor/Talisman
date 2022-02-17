<template>
  <div id="first" class="main__right__first">
    <div class="main__right__first__text">
      <h1>
      Идеальное<br />
      пространство<br />
      <span>для жизни</span>
    </h1>
      <p>
        Многоквартирный жилой комплекс премиум<br />
        класса в городе ТАРАЗ
      </p>
    </div>
    
    <div class="main__right__first__slider">
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
</template>

<script>
import {Slider, SliderItem} from 'vue-easy-slider'

export default {
    name: "FirstComponent",
    components: {
      Slider,
      SliderItem
    },
    data() {
      return {
        sliderIndex: 0,
        galleryList: [
                {
                    id: 1,
                    url: "/01.png"
                },
                {
                    id: 2,
                    url: "/02.png"
                },
                {
                    id: 3,
                    url: "/03.png"
                },
                {
                    id: 4,
                    url: "/04.png"
                },
                {
                    id: 5,
                    url: "/05.jpg"
                },
                {
                    id: 6,
                    url: "/06.jpg"
                },
                {
                    id: 7,
                    url: "/07.jpg"
                }
            ]
      }
    }
}
</script>