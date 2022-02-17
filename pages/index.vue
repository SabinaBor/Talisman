<template>
<div>
  <FirstComponent />
  <SecondComponent />
  <ThirdComponent />
  <FourthComponent />
  <EightComponent />
  <FifthComponent />
  <SixthComponent />
  <SeventhComponent />
  <NinthComponent />
</div>
</template>

<script>
import FirstComponent from "@/components/First";
import SecondComponent from "@/components/Second";
import ThirdComponent from "@/components/Third";
import FourthComponent from "@/components/Fourth";
import FifthComponent from "@/components/Fifth";
import SixthComponent from "@/components/Sixth";
import SeventhComponent from "@/components/Seventh";
import EightComponent from "@/components/Eight";
import NinthComponent from "@/components/Ninth";

export default {
  name: 'IndexPage',
  components: {
    FirstComponent,
    SecondComponent,
    ThirdComponent,
    FourthComponent,
    FifthComponent,
    SixthComponent,
    SeventhComponent,
    EightComponent,
    NinthComponent
  },
  data() {
    return {
      list: [
        { backgroundColor: '#3f51b5', width: '500px', height: '200px' },
        { backgroundColor: '#eee', width: '500px', height: '200px' },
        { backgroundColor: '#f44336', width: '500px', height: '200px' },
      ]
    }
  }
}
</script>

<style lang="scss">
* {
  &::-webkit-scrollbar {
    display: none;
  }
}

.main {
  span.title {
    color: #C2A582;
    font-size: 12px;
    text-transform: uppercase;
    @media screen and (min-width: 1600px) and (min-height: 700px) {
      font-size: 16px;
    }
  }
  &__right {
    &__first {
      height: 100vh;
      padding: 40px 0 0 80px;
      @media screen and (min-width: 1600px) and (min-height: 700px) {
        padding: 60px 0 0 100px;
      }
      &__text {
        width: fit-content;
        position: relative;
        padding: 12px;
        z-index: 1000;
        background: #5f4526cf;
      }
      &__slider {
        position: absolute;
        top: 0;
        left: 100px;
        width: calc(100vw - 100px);
        height: 100vh;
        .slider {
          height: 100%!important;
          width: 100%!important;
          &-btn {
            display: none!important;;
          }
          &-item {
            .img__wrapper {
              width: 100%!important;
              height: 100%!important;
              display: flex;
              justify-content: center;
              align-items: center;
              position: absolute;
              top: 0;
              left: 0;
              img {
                width: 100%;
              }
            }
          }
        }
      }
      h1, p {
        font-family: "FiraSans-Regular";
        color: #fff;
        position: relative;
        z-index: 100000;
      }
      p {
        font-size: 12px;
        @media screen and (min-width: 1600px) and (min-height: 700px) {
          font-size: 24px;
        }
      }
      h1 {
        font-size: 36px;
        text-transform: uppercase;
        line-height: 44px;
        letter-spacing: 0.36px;
        @media screen and (min-width: 1600px) and (min-height: 700px) {
          font-size: 48px;
        }
        span {
          font-family: "FiraSans-SemiBold";
        }
      }
    }
    &__second {
      display: flex;
      height: 100vh;
      &__text {
        display: flex;
        margin: 0 auto;
        flex-direction: column;
        padding-top: 40px;
        padding-left: 100px;
        width: 50%;
        @media screen and (min-width: 1600px) and (min-height: 700px) {
          padding-top: 80px;
          padding-left: 120px;
        }
        span.title {
          margin-bottom: 36px;
        }
        h2, h3, p {
          text-align: left;
          letter-spacing: 1px;
          margin-bottom: 12px;
          @media screen and (min-width: 1600px) and (min-height: 700px) {
            margin-bottom: 20px;
          }
        }
        h2 {
          font-size: 24px;
          font-family: "FiraSans-Regular";
          &.semibold {
            font-family: "FiraSans-SemiBold";
          }
          @media screen and (min-width: 1600px) and (min-height: 700px) {
            font-size: 28px;
          }
        }
        h2, h3 {
          color: #5F4526;
          line-height: 20px;
        }
        h3, p {
          font-family: "FiraSans-Regular";
        }
        h3 {
          font-size: 16px;
          text-transform: uppercase;
          @media screen and (min-width: 1600px) and (min-height: 700px) {
            font-size: 20px;
          }
        }
        p {
          font-size: 12px;
          color: #4D4D4D;
          line-height: 1.4vw;
          letter-spacing: 0.14px;
          @media screen and (min-width: 1600px) and (min-height: 700px) {
            font-size: 16px;
          }
        }
      }
      &__image {
        width: 50%;
        background: url("../static/03.png") no-repeat 0 center;
        background-size: cover;
      }
    }
    &__third {
      background: linear-gradient(-58.06deg, rgba(167, 149, 84, 1) 0%, rgba(249, 197, 58, 1) 100%);;
      padding: 40px 8vw;
      span.title {
        color: #fff;
      }
    }
    &__fourth {
      &__image {
        background: url("../static/04.png") no-repeat 0 center;
        background-size: cover;
      }
    }
    &__fifth {
      background: #B0A99E;
    }
    &__sixth {
      background: #F5EDE2;
    }
    &__seventh {
      background: #565044;
    }
    &__ninth {
      background: #5F4526;
    }
  }
}

.full-height {
  height: 100vh;
}
</style>
