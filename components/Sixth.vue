<template>
  <div id="sixth" class="main__right__sixth full-height">
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
  name: "SixthComponent",
  components: {
    Slider,
    SliderItem
  },
  data() {
    return {
      sliderIndex: 0,
      imageList: [
        {
          id: 1,
          url: '/six.png'
        },
        {
          id: 2,
          url: '/seventh.png'
        },
        {
          id: 3,
          url: '/eight.png'
        },
        {
          id: 4,
          url: '/nine.png'
        }
      ],
    }
  }
}
</script>

<style lang="scss">
  .container {
    width: 600px;
    height: 400px;
    .slider {
      width: 100%!important;
      height: 100%!important;
      img {
        width: 100%;
      }
    }
  }
</style>
