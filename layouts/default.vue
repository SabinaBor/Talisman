<template>
    <div class="main">
        <div @click="menuActive=!menuActive" class="main__left" :class="{'active': menuActive}">
            <Logo />
          <div class="main__left__item">
            <div class="main__menu">
              <div class="main__menu__dot"
                   v-for="i in 8" :key="i + 'a'"
                   :class="{'active': scrollYPos < windowHeight*(i) && scrollYPos >= windowHeight*(i - 1)}">
                <div class="circle"></div>
              </div>
            </div>
            <div class="main__menu" :class="{'show': menuActive}">
              <div class="main__menu__subtitle" v-for="(sub, id) in subtitleMenu" :key="id + 'b'">
                {{sub.name}}
              </div>
            </div>
          </div>
        </div>
        <div class="main__right">
            <Nuxt />
        </div>
    </div>
</template>

<script>
import Logo from "@/components/svg/Logo";

export default {
    name: "DefaultLayout",
    components: {
        Logo
    },
    data() {
        return {
          scrollYPos: 0,
          menuActive: false,
          subtitleMenu: [
            {
              id: 1,
              name: "Home"
            },
            {
              id: 2,
              name: "О проекте"
            },
            {
              id: 3,
              name: "Галерея"
            },
            {
              id: 4,
              name: "Инфраструктура"
            },
            {
              id: 5,
              name: "КОММЕРЦИЯ"
            },
            {
              id: 6,
              name: "Квартиры"
            },
            {
              id: 7,
              name: "Планировка"
            },
            {
              id: 8,
              name: "Контакты"
            }
          ]
        }
    },
    mounted() {
      window.addEventListener("scroll", this.scrollHandle);
    },
    destroyed () {
      window.removeEventListener("scroll", this.scrollHandle);
    },
    computed: {
        windowHeight() {
            return window.innerHeight;
        }
    },
    methods: {
        scrollHandle() {
            this.scrollYPos = window.scrollY;
        },
    }
}
</script>

<style lang="scss">

@keyframes showMenu {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.main {
    &__left {
        background: #fff;
        padding: 40px 20px;
        display: flex;
        flex-direction: column;
        position: fixed;
        width: 100px;
        height: 100vh;
        top: 0;
        left: 0;
        transition: 1s all;
        &>svg {
          width: 60px;
        }
        &.active {
          width: 590px;
        }
      &__item {
        display: flex;
        margin-top: 100px;
        align-items: flex-start;
      }
    }
    &__right {
        margin-left: 100px;
    }
    &__menu {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding-left: 23px;
        width: fit-content;
      &:nth-child(2) {
        align-items: flex-start;
        margin-left: 100px;
        opacity: 0;
        animation: none;
        transition: opacity 0.2s linear;
        &.show {
          opacity: 1;
          transition: opacity 1s ease-in-out;
          //animation: 0.5s linear showMenu;
          //animation-delay: 0.2s;
          //animation-fill-mode: forwards;
        }
      }
        &__dot {
            border: 2px solid #A3A3A3;
            border-radius: 50%;
            width: 10px;
            height: 10px;
            margin-bottom: 14px;
            display: flex;
            justify-content: center;
            align-items: center;
            &:hover {
                cursor: pointer;
            }
          &.active {
            border-color: #5F4526;
            width: 14px;
            height: 14px;
            .circle {
              background: #5F4526;
              width: 7px;
              height: 7px;
              border-radius: 50%;
            }
          }
        }
    }
}
</style>
