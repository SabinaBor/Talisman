<template>
<div>
  <FirstComponent />
  <SecondComponent />
  <ThirdComponent />
  <FourthComponent />
  <FifthComponent />
  <SixthComponent />
  <SeventhComponent />
  <!-- <EightComponent /> -->
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
.main {
  span.title {
    color: #C2A582;
    font-size: 0.72vw;
    text-transform: uppercase;
  }
  &__right {
    &__first {
      background: url("../assets/images/1x/first.png");
      background-repeat: no-repeat;
      background-size: cover;
      background-position: center;
      height: 100vh;
      padding: 40px 0 0 8vw;
      h1, p {
        font-family: "FiraSans-Regular";
        color: #fff
      }
      p {
        font-size: 1.2vw;
      }
      h1 {
        font-size: 2.4vw;
        text-transform: uppercase;
        line-height: 44px;
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
        padding-left: 8vw;
        width: 50%;
        span.title {
          margin-bottom: 4vw;
        }
        h2, h3, p {
          text-align: left;
          letter-spacing: 1px;
          margin-bottom: 1.2vw;
        }
        h2 {
          font-size: 2vw;
          font-family: "FiraSans-Regular";
          &.semibold {
            font-family: "FiraSans-SemiBold";
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
          font-size: 1.2vw;
          text-transform: uppercase;
        }
        p {
          font-size: 0.8vw;
          color: #4D4D4D;
        }
      }
      &__image {
        width: 50%;
        background: url("../assets/images/1x/third.png");
        background-size: cover;
        background-position: 0 center;
        background-repeat: no-repeat;
      }
    }
    &__third {
      background: #A79554;
    }
    &__fourth {
      &__image {
        background: url("../assets/images/1x/fourth.png");
        background-size: cover;
        background-position: 0 center;
        background-repeat: no-repeat;
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