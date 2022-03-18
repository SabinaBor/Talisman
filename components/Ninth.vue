<template>
  <div id="eightth" class="main__right__ninth full-height">
    <div class="contacts">
      <div class="img__wrapper">
        <div class="contacts__top">
          <h3>ЗАКАЖИТЕ ЗВОНОК!</h3>
          <p>Мы свяжемся с вами и ответим на все ваши вопросы</p>
          <div class="contacts__top__form">
            <input type="text" v-model="name" placeholder="Имя" />
            <input
              type="text"
              v-model="phone_number"
              placeholder="Номер телефона: +7"
            />
            <button class="contacts__top__form__btn">
              <img src="../assets/images/arrow-right_yellow.svg" alt="image" />
            </button>
          </div>
        </div>
      </div>
      <div class="contacts__middle">
        <div class="contacts__middle__left">
          <p>НАШИ КОНТАКТЫ</p>
          <p>моб: +7 777 393 2222</p>
          <p>тел: +7 724 393 2222</p>
          <p>email: talisman@taraz.kz</p>
        </div>
        <div class="contacts__middle__right"></div>
      </div>
      <div class="contacts__bottom">
        <div class="contacts__bottom__links">
          <div class="facebook-link">
            <img src="../assets/images/facebook.svg" alt="facebook" />
            <div class="arrow-right">
              <img src="../assets/images/arrow-right_white.svg" alt="arrow" />
            </div>
          </div>
          <div class="instagram-link">
            <img src="../assets/images/instagram.svg" alt="instagram" />
            <div class="arrow-right">
              <img src="../assets/images/arrow-right_white.svg" alt="arrow" />
            </div>
          </div>
        </div>
        <p>©2021-2022 TALISMAN RESIDENTIAL COMPLEX. Все права защищены.</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NinthComponent",
};
</script>

<style lang="scss" scoped>
.main__right__ninth {
  position: relative;
  @media only screen and (max-width: 1025px) {
    padding: 0;
  }
  .contacts {
    height: 100%;
    width: 100%;
    .img__wrapper {
      background: url("../assets/images/hands.png");
      height: 50%;
      background-repeat: no-repeat;
      width: 100%;
      background-size: cover;
      background-position: center;
      @media only screen and (max-width: 1025px) {
        height: auto;
      }
    }
    &__top {
      background: rgba(47, 94, 57, 0.85);
      height: 100%;
      width: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      @media only screen and (max-width: 1025px) {
        height: 100%;
        padding: 50px 28px;
      }
      h3 {
        font-size: 48px;
        font-weight: 700;
        color: #fff;
        letter-spacing: 0.46px;
        margin-bottom: 16px;
        @media only screen and (max-width: 1025px) {
          font-size: 20px;
        }
      }
      p {
        font-size: 18px;
        margin-bottom: 32px;
        color: #fff;
        @media only screen and (max-width: 1025px) {
          font-size: 12px;
          text-align: center;
          margin-bottom: 20px;
        }
      }
      &__form {
        width: 50%;
        display: flex;
        @media only screen and (max-width: 1025px) {
          flex-direction: column;
          width: 100%;
        }
        input {
          width: 50%;
          height: 50px;
          font-size: 14px;
          padding-left: 16px;
          @media only screen and (max-width: 1025px) {
            width: 100%;
            margin-bottom: 20px;
            font-size: 12px;
          }
        }
        button {
          width: 50px;
          height: 50px;
          padding: 0;
          border: none;
          @media only screen and (max-width: 1025px) {
            margin: 0 auto;
            width: 120px;
            background: #f9c53a;
          }
          img {
            height: 100%;
          }
        }
      }
    }
    &__middle {
      height: 30%;
      background: #45321c;
      display: flex;
      align-items: center;
      @media only screen and (max-width: 1025px) {
        height: auto;
        width: 100%;
        display: block;
      }
      &__left {
        height: 100%;
        width: 30%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        padding: 16px 16px 16px 64px;
        @media only screen and (max-width: 1025px) {
          width: 100%;
          padding: 20px 28px;
        }
        p {
          font-size: 16px;
          color: #fff;
          margin-bottom: 8px;
          font-weight: 300;
          letter-spacing: 0.05em;
          @media only screen and (max-width: 1025px) {
            width: 100%;
            text-align: center;
            font-size: 14px;
          }
          &:first-child {
            font-weight: 600;
            font-size: 18px;
            margin-bottom: 16px;
          }
        }
      }
      &__right {
        height: 100%;
        width: 70%;
        background: beige;
      }
    }
    &__bottom {
      height: 20%;
      padding-top: 16px;
      @media only screen and (max-width: 1025px) {
        padding: 0;
      }
      &__links {
        display: flex;
        align-items: center;
        height: 60%;
        @media only screen and (max-width: 1025px) {
          flex-direction: column;
        }
        .facebook-link,
        .instagram-link {
          width: 50%;
          display: flex;
          justify-content: space-between;
          align-items: center;
          height: 100%;
          padding-left: 64px;
          @media only screen and (max-width: 1025px) {
            width: 100%;
            height: 80px;
            padding: 0 0 0 28px;
          }
          &:hover {
            cursor: pointer;
            background: #45321c;
            transition: 0.1s all linear;
          }
          img {
            width: 150px;
            @media only screen and (max-width: 1025px) {
              padding: 28px 0;
            }
          }
          .arrow-right {
            height: 100%;
            display: flex;
            align-items: center;
            width: 60px;
            justify-content: center;
            background: #ffffff1a;
            img {
              width: 16px;
            }
          }
        }
        .facebook-link {
          background: #3e5193;
        }
        .instagram-link {
          background: #bb1d1d;
        }
        & + p {
          margin-bottom: 0;
          color: #fff;
          font-size: 14px;
          height: 40%;
          display: flex;
          align-items: center;
          padding-left: 64px;
          @media only screen and (max-width: 1025px) {
            font-size: 8px;
            padding: 28px;
          }
        }
      }
    }
  }
}
</style>
