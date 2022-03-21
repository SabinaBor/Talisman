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
  name: "IndexPage",
  components: {
    FirstComponent,
    SecondComponent,
    ThirdComponent,
    FourthComponent,
    FifthComponent,
    SixthComponent,
    SeventhComponent,
    EightComponent,
    NinthComponent,
  },
  data() {
    return {
      list: [
        { backgroundColor: "#3f51b5", width: "500px", height: "200px" },
        { backgroundColor: "#eee", width: "500px", height: "200px" },
        { backgroundColor: "#f44336", width: "500px", height: "200px" },
      ],
    };
  },
};
</script>

<style lang="scss">
* {
  &::-webkit-scrollbar {
    display: none;
  }
}

.main {
  @media only screen and (max-width: 1025px) {
    width: 100%;
    overflow: hidden;
  }
  span.title {
    color: #c2a582;
    font-size: 12px;
    text-transform: uppercase;
    @media screen and (min-width: 1600px) and (min-height: 700px) {
      font-size: 16px;
    }
  }
  &__right {
    @media only screen and (max-width: 1025px) {
      margin: 0;
      width: 100%;
    }
    &__first {
      height: 100vh;
      padding: 40px 0 0 80px;
      @media screen and (min-width: 1600px) and (min-height: 700px) {
        padding: 60px 0 0 100px;
      }
      @media only screen and (max-width: 1025px) {
        width: 100vw;
        height: 300px;
        position: relative;
        padding: 16px 0 0 66px;
      }
      @media only screen and (max-width: 450px) {
        height: 250px;
      }
      &__text {
        width: fit-content;
        position: relative;
        padding: 12px;
        z-index: 1000;
        // background: #5f4526cf;
        @media only screen and (max-width: 1025px) {
          top: 0;
          left: 0;
          width: 84%;
        }
      }
      &__slider {
        position: absolute;
        top: 0;
        left: 100px;
        width: calc(100vw - 100px);
        height: 100vh;
        @media only screen and (max-width: 1025px) {
          width: 100vw;
          height: fit-content;
          left: 0;
        }
        .slider {
          height: 100% !important;
          width: 100% !important;
          @media only screen and (max-width: 1025px) {
            height: 300px !important;
          }
          @media only screen and (max-width: 450px) {
            height: 250px !important;
          }
          .slider-indicator-icon {
            @media only screen and (max-width: 1025px) {
              border: 2px solid #fff !important;
              margin: 0 8px !important;
            }
          }
          &-btn {
            display: none !important;
          }
          &-item {
            .img__wrapper {
              width: 100% !important;
              height: 100% !important;
              display: flex;
              justify-content: center;
              align-items: center;
              position: absolute;
              top: 0;
              left: 0;
              img {
                height: 100%;
                width: 100%;
              }
            }
          }
        }
      }
      h1,
      p {
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
        @media only screen and (max-width: 1025px) {
          width: 72%;
          font-size: 10px;
          margin: 0;
          br {
            display: none;
          }
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
        @media only screen and (max-width: 1025px) {
          font-size: 20px;
          line-height: initial;
          letter-spacing: initial;
          width: fit-content;
        }
        span {
          font-family: "FiraSans-SemiBold";
        }
      }
    }
    &__second {
      display: flex;
      height: 100vh;
      @media only screen and (max-width: 1025px) {
        flex-direction: column;
        width: 100%;
        height: auto;
        padding: 0!important;
      }
      @media only screen and (min-height: 680px) and (max-width: 850px) {
        height: calc(100vh - 300px);
      }
      @media only screen and (max-width: 450px) {
        width: 100%;
      }
      @media only screen and (max-height: 680px) and (max-width: 450px) {
        height: auto;
      }
      @media only screen and (min-height: 680px) and (max-width: 450px) {
        height: calc(100vh - 250px);
      }
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
        @media only screen and (max-width: 1025px) {
          padding: 40px 0;
          width: 80%;
        }
        @media only screen and (max-width: 850px) {
          padding: 16px 28px;
          width: 100%;
          height: calc(100vh - 250px);
          margin: 0;
        }
        span.title {
          margin-bottom: 36px;
          @media only screen and (max-width: 1025px) {
            margin-bottom: 8px;
          }
        }
        h2,
        h3,
        p {
          text-align: left;
          letter-spacing: 1px;
          margin-bottom: 12px;
          @media screen and (min-width: 1600px) and (min-height: 700px) {
            margin-bottom: 20px;
          }
          @media only screen and (max-width: 1025px) {
            margin-bottom: 8px;
            line-height: initial !important;
            letter-spacing: initial !important;
          }
        }
        h2 {
          font-size: 24px;
          font-family: "FiraSans-Regular";
          @media only screen and (max-width: 850px) {
            font-size: 20px;
          }
          &.semibold {
            font-family: "FiraSans-SemiBold";
            @media only screen and (max-width: 850px) {
              margin-bottom: 0;
            }
          }
          @media screen and (min-width: 1600px) and (min-height: 700px) {
            font-size: 28px;
          }
        }
        h2,
        h3 {
          color: #5f4526;
          line-height: 20px;
        }
        h3,
        p {
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
          color: #4d4d4d;
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
        @media only screen and (max-width: 850px) {
          height: 400px;
          width: 100%;
        }
      }
    }
    &__third {
      background: linear-gradient(
        -58.06deg,
        rgba(167, 149, 84, 1) 0%,
        rgba(249, 197, 58, 1) 100%
      );
      padding: 40px 8vw;
      @media only screen and (max-width: 1025px) {
        height: auto !important;
      }
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
      background: #b0a99e;
    }
    &__sixth {
      background: #f5ede2;
    }
    &__seventh {
      background: #565044;
    }
    &__ninth {
      background: #5f4526;
    }
  }
}

.full-height {
  height: 100vh;
  @media only screen and (max-width: 850px) {
    height: auto;
  }
  @media only screen and (max-width: 850px) {
    padding: 12px 28px 40px;
  }
}
</style>
