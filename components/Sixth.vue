<template>
  <div id="sixth" class="main__right__second main__right__sixth">
    <div class="main__right__second__text">
      <span class="title">КВАРТИРЫ</span>
      <h2 class="semibold">КВАРТИРЫ</h2>
      <h2>В КОМПЛЕКСЕ ТАЛИСМАН</h2>
      <p>
        На территории комплекса TALISMAN есть ко-<br/>
        фейня, супермаркет, салон красоты, ресторан<br/>
        и многое другое. Также в доступности распо-<br/>
        ложены крупные строительные магазины,<br/>
        дошкольные образовательные центры, архе-<br/>
        ологический парк.
      </p>
      <h3>СТИЛЬ</h3>
      <p>
        В жилом комплексе TALISMAN предусмотрен<br/>
        просторный одноэтажный подземный паркинг–<br/>
        благодаря этому внутренние дворы и терри-<br/>
        тория комплекса не будут заставлены<br/>
        машинами. Такое преимущество станет<br/>
        немаловажным при выборе ЖК для семей,<br/>
        где есть дети и пожилые родители,
      </p>
      <h3>ПРОСТРАНСТВО</h3>
      <p>
        Внутренние дворы комплекса спроектирова-<br/>
        ны как закрытая, приватная территория для<br/>
        жителей, с контролируемым доступом по<br/>
        электронному ключу и системой Face ID.
      </p>
    </div>
    <div class="main__right__second__image main__right__sixth__image">
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
    name: "SixthComponent",
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
                }
            ]
      }
    }
}
</script>

<style lang="scss">
.main__right__sixth {
  &__image {
    background: none;
    .slider {
      width: 100%!important;
      height: 100%!important;
      img {
        width: 100%;
        height: 100%;
      }
    }
  }
}
</style>