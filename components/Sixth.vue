<template>
  <div class="main__right__sixth full-height">
    <span class="title">Квартиры</span>
    <div class='container'>
      <client-only>
        <slider
          v-model='sliderIndex'
          animation="fade"
          stop-on-hover
          :interval='6000'
        >
            <slider-item v-for="(image, index) in imageList" :key="index">
              <div class="img__wrapper">
                <img :src="image" />
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
  name: "SixthComponent",
  components: {
    Slider,
    SliderItem
  },
  data() {
    return {
      sliderIndex: 0,
      imageList: [
        '/_nuxt/assets/images/1x/six.png',
        '/_nuxt/assets/images/1x/seventh.png',
        '/_nuxt/assets/images/1x/eight.png',
        '/_nuxt/assets/images/1x/nine.png'
      ],
    }
  }
}
</script>

<style lang="scss">
  .container {
    width: 600px;
    height: 600px;
  }
</style>
