<template>
  <div class="main">
    <div
      @click="menuActive = !menuActive"
      class="main__left"
      :class="[{ active: menuActive }, { 'show-mobile': showMobileMenu }]"
    >
      <Logo />
      <div class="main__left__item">
        <div class="main__menu">
          <!-- <div class="main__menu__dot"
                   v-for="i in 8" :key="i + 'a'"
                   :class="{'active': 
                   (scrollYPos < windowHeight*(i) && scrollYPos >= windowHeight*(i - 1) && i < 4)
                   || (scrollYPos < windowHeight*(i+1) && scrollYPos >= windowHeight*(i-1) && i === 4)
                   || (scrollYPos < windowHeight*(i+1) && scrollYPos >= windowHeight*(i) && i > 4)
                   }">
                <div class="circle"></div>
              </div> -->
        </div>
        <div class="main__menu" :class="{ show: menuActive }">
          <a
            :href="sub.idUrl"
            v-for="(sub, id) in subtitleMenu"
            :key="id + 'b'"
          >
            <div
              class="main__menu__subtitle"
              :class="{
                active:
                  scrollYPos < windowHeight * (id + 1) &&
                  scrollYPos >= windowHeight * id,
              }"
            >
              <div class="main__menu__dot">
                <div class="circle"></div>
              </div>
              {{ sub.name }}
            </div>
          </a>
        </div>
      </div>
      <div class="main__left__download">
        <div class="main__left__download__rectangle"></div>
        <a href="/Планировка_Талисман.zip" download="Планировка_Талисман">
          <div class="main__left__download__text" :class="{ show: menuActive }">
            СКАЧАТЬ ПЛАНИРОВКУ КВАРТИР
          </div>
        </a>
      </div>
    </div>
    <div class="main__right" @click="menuActive = false">
      <Nuxt />
    </div>
    <div
      class="main__menu_mobile mobile"
      :class="{ rotated: showMobileMenu }"
      @click="showMobileMenu = !showMobileMenu"
    >
      <div>
        <hr />
        <hr />
        <hr />
      </div>
    </div>
  </div>
</template>

<script>
import Logo from "@/components/svg/Logo";

export default {
  name: "DefaultLayout",
  components: {
    Logo,
  },
  data() {
    return {
      scrollYPos: 0,
      menuActive: false,
      showMobileMenu: false,
      subtitleMenu: [
        {
          id: 1,
          name: "Home",
          idUrl: "#first",
        },
        {
          id: 2,
          name: "О проекте",
          idUrl: "#second",
        },
        {
          id: 3,
          name: "Галерея",
          idUrl: "#third",
        },
        {
          id: 4,
          name: "Инфраструктура",
          idUrl: "#fourth",
        },
        {
          id: 5,
          name: "КОММЕРЦИЯ",
          idUrl: "#fifth",
        },
        {
          id: 6,
          name: "Квартиры",
          idUrl: "#sixth",
        },
        {
          id: 7,
          name: "Планировка",
          idUrl: "#seventh",
        },
        {
          id: 8,
          name: "Контакты",
          idUrl: "#eightth",
        },
      ],
    };
  },
  mounted() {
    window.addEventListener("scroll", this.scrollHandle);
    document.querySelectorAll('a[href^="#"]').forEach((anchor) => {
      anchor.addEventListener("click", function (e) {
        e.preventDefault();
        document.querySelector(this.getAttribute("href")).scrollIntoView({
          behavior: "smooth",
        });
      });
    });
  },
  destroyed() {
    window.removeEventListener("scroll", this.scrollHandle);
  },
  computed: {
    windowHeight() {
      return window.innerHeight;
    },
  },
  methods: {
    scrollHandle() {
      this.scrollYPos = window.scrollY;
      this.menuActive = false;
    },
  },
};
</script>

<style lang="scss">
@media only screen and (max-width: 850px) {
  br {
    display: none;
  }
}

a {
  text-decoration: none;
  outline: none;
  color: transparent;
  &:hover {
    text-decoration: none;
  }
}

@keyframes showMenu {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.main {
  &__menu_mobile {
    position: fixed;
    top: 0;
    left: 0;
    width: 40px;
    height: 40px;
    background: #5f4526;
    z-index: 100000;
    div {
      box-sizing: border-box;
      display: flex !important;
      justify-content: center;
      align-items: center;
      row-gap: 4px;
      flex-direction: column;
      width: 100%;
      height: 100%;
    }
    &.rotated {
      background: #d4d4d4;
      div {
        transform: rotate(-45deg);
      }
    }
    hr {
      margin: 0px;
      border-top: 1px solid #fff;
      width: 50%;
    }
  }
  &__left {
    z-index: 10000;
    background: #fff;
    padding: 40px 0;
    display: flex;
    flex-direction: column;
    position: fixed;
    width: 100px;
    height: 100vh;
    top: 0;
    left: 0;
    transition: 1s all;
    border-right: 1px solid #a3a3a3;
    @media only screen and (max-width: 850px) {
      width: 100%;
      display: none;
    }
    &.show-mobile {
      @media only screen and (max-width: 850px) {
        display: flex;
      }
    }
    & > svg {
      width: 60px;
      margin-left: 20px;
      @media only screen and (max-width: 1025px) {
        margin: 0 auto;
        width: 80px;
      }
    }
    &.active {
      width: 590px;
    }
    &__item {
      display: flex;
      margin-top: 100px;
      align-items: flex-start;
      @media only screen and (max-width: 1025px) {
        margin-top: 32px;
      }
    }
    &__download {
      display: flex;
      align-items: center;
      margin-top: auto;
      margin-bottom: 24px;
      padding: 15px 0 15px 42.5px;
      transition: all 0.3s ease-in-out;
      &__rectangle {
        border: 2px solid #a3a3a3;
        border-radius: 2px;
        width: 15px;
        height: 20px;
        min-width: 15px;
      }
      &__text {
        margin-left: 100px;
        white-space: nowrap;
        opacity: 0;
        transition: opacity 0.2s linear;
        padding-left: 0;
        font-size: 14px;
        color: #a3a3a3;
        text-transform: uppercase;
        font-family: "FiraSans-Regular";
        letter-spacing: 0.2em;
        @media screen and (min-width: 1600px) and (min-height: 700px) {
          font-size: 20px;
          margin-left: 60px;
        }
        &.show {
          opacity: 1;
          transition: opacity 1s ease-in-out;
          width: 100%;
        }
      }
      &:hover {
        cursor: pointer;
        background: #c2a582;
        .main__left__download__text {
          color: #fff;
        }
        .main__left__download__rectangle {
          border-color: #fff;
        }
      }
      @media only screen and (max-width: 850px) {
        .main__left__download {
          background: #c2a582;
          &__text {
            opacity: 1;
            font-size: 10px;
            margin-left: 34px;
          }
        }
      }
    }
  }
  &__right {
    margin-left: 100px;
  }
  &__menu {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-left: 0;
    width: fit-content;
    justify-content: space-between;
    height: 100%;
    a {
      width: 100%;
    }
    &:first-child {
      padding-top: 8px;
    }
    &:nth-child(2) {
      align-items: flex-start;
      opacity: 1;
      overflow: hidden;
      animation: none;
      padding-left: 39px;
      transition: opacity 0.2s linear;
      height: calc(100% + 8px);
      @media screen and (min-width: 1600px) and (min-height: 700px) {
        margin-left: 60px;
      }
      &.show {
        opacity: 1;
        transition: opacity 1s ease-in-out;
        width: 100%;
      }
    }
    &__subtitle {
      font-size: 14px;
      color: #a3a3a3;
      text-transform: uppercase;
      font-family: "FiraSans-Regular";
      letter-spacing: 0.2em;
      display: flex;
      white-space: nowrap;
      display: flex;
      justify-content: flex-start;
      width: 100%;
      column-gap: 100px;
      margin-bottom: 12px;
      align-items: center;
      @media screen and (min-width: 1600px) and (min-height: 700px) {
        font-size: 20px;
      }
      @media only screen and (max-width: 850px) {
        column-gap: 40px;
      }
      &:hover {
        cursor: pointer;
        color: #5f4526;
        font-family: "FiraSans-SemiBold";
      }
      &.active {
        color: #5f4526;
        margin-left: -6px;
        column-gap: 94px;
        @media only screen and (max-width: 850px) {
          column-gap: 34px;
        }
        &::after {
          content: " ";
          width: 100%;
          content: "";
          border-top: 1px solid #5f4526;
          margin-left: 24px;
        }
        .main__menu__dot {
          border-color: #5f4526;
          width: 22px;
          min-width: 22px;
          height: 22px;
          .circle {
            background: #5f4526;
            width: 10px;
            height: 10px;
            min-width: 10px;
            border-radius: 50%;
          }
        }
      }
    }
    &__dot {
      border: 2px solid #a3a3a3;
      border-radius: 50%;
      width: 10px;
      height: 10px;
      min-width: 10px;
      margin-bottom: 14px;
      display: flex;
      justify-content: center;
      align-items: center;
      @media screen and (min-width: 1600px) and (min-height: 700px) {
        margin-bottom: 32px;
      }
      &:last-child {
        margin-bottom: 0;
      }
      &:hover {
        cursor: pointer;
      }
    }
  }
}
</style>
