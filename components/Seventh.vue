<template>
  <div id="seventh" class="main__right__seventh full-height">
    <div class="main__right__seventh__items">
      <div class="main__right__seventh__item">
        <div class="main__right__seventh__item__top">
          <div class="img__wrapper">
            <img src="../assets/images/arrow-right.svg" alt="arrow-right" />
          </div>
          <div class="apartment-type">
            <p>ПЛАНИРОВКА</p>
            <span>2-Х КВ.</span>
          </div>
        </div>
        <div class="main__right__seventh__item__bottom">
          <p class="white">2-Х КВАРТИР:</p>
          <p class="gray">БЛОК A: 14</p>
          <p class="gray">БЛОК B: 14</p>
          <p class="gray">БЛОК C: 14</p>
          <p class="white">ПЛОЩАДЬ: от 62 м<sup>2</sup></p>
          <p class="white">ЦЕНА: от 702 000 тг. за м<sup>2</sup></p>
        </div>
      </div>
      <div class="main__right__seventh__item">
        <div class="main__right__seventh__item__top">
          <div class="img__wrapper">
            <img src="../assets/images/arrow-right.svg" alt="arrow-right" />
          </div>
          <div class="apartment-type">
            <p>ПЛАНИРОВКА</p>
            <span>3-Х КВ.</span>
          </div>
        </div>
        <div class="main__right__seventh__item__bottom">
          <p class="white">3-Х КВАРТИР:</p>
          <p class="gray">БЛОК A: 37</p>
          <p class="gray">БЛОК B: 37</p>
          <p class="gray">БЛОК C: 37</p>
          <p class="white">ПЛОЩАДЬ: от 75 м<sup>2</sup></p>
          <p class="white">ЦЕНА: от 650 000 тг. за м<sup>2</sup></p>
        </div>
      </div>
      <div class="main__right__seventh__item">
        <div class="main__right__seventh__item__top">
          <div class="img__wrapper">
            <img src="../assets/images/arrow-right.svg" alt="arrow-right" />
          </div>
          <div class="apartment-type">
            <p>ПЛАНИРОВКА</p>
            <span>4-Х КВ.</span>
          </div>
        </div>
        <div class="main__right__seventh__item__bottom">
          <p class="white">4-Х КВАРТИР:</p>
          <p class="gray">БЛОК A: 21</p>
          <p class="gray">БЛОК B: 21</p>
          <p class="gray">БЛОК C: 21</p>
          <p class="white">ПЛОЩАДЬ: от 105 м<sup>2</sup></p>
          <p class="white">ЦЕНА: от 602 000 тг. за м<sup>2</sup></p>
        </div>
      </div>
    </div>
    <div class="download-plan">Скачать планировку квартир (PDF, 18kb)</div>
  </div>
</template>

<script>
export default {
  name: "SeventhComponent",
};
</script>

<style lang="scss" scoped>
.main__right__seventh {
  position: relative;
  @media only screen and (max-width: 1025px) {
    padding: 12px 28px 60px;
  }
  &__items {
    display: flex;
    margin: 0 auto;
    width: 100%;
    padding: 80px 70px;
    flex-wrap: wrap;
    justify-content: center;
    @media only screen and (max-width: 1025px) {
      flex-direction: column;
      padding: 0;
    }
  }
  &__item {
    width: calc(100% / 3 - 70px);
    @media only screen and (max-width: 1025px) {
      width: 100%;
      margin-top: 40px;
    }
    &__top {
      margin-bottom: 32px;
      display: flex;
      border: 1px solid #fff;
      align-items: center;
      padding: 20px;
      .img__wrapper {
        height: 20px;
        width: 20px;
        margin-right: 20px;
        img {
          height: 100%;
          width: 100%;
        }
      }
      .apartment-type {
        p {
          font-size: 18px;
          letter-spacing: 0.45px;
          color: #fff;
          font-weight: 400;
          margin-bottom: 0;
        }
        span {
          font-weight: 700;
          font-size: 18px;
          letter-spacing: 0.45px;
          color: #f9c53a;
        }
      }
      &:hover {
        background: rgba(249, 197, 58, 0.5);
        cursor: pointer;
        .apartment-type p {
          color: #f9c53a;
        }
      }
    }
    &__bottom {
      width: 80%;
      @media only screen and (max-width: 1025px) {
        width: 100%;
      }
      p {
        &.white {
          font-size: 14px;
          letter-spacing: 0.45px;
          color: #fff;
          border-bottom: 1px solid #fff;
          padding: 16px 0;
          margin-bottom: 0;
        }
        &.gray {
          font-size: 14px;
          letter-spacing: 0.9px;
          color: rgba(255, 255, 255, 0.6);
          border-bottom: 1px solid #fff;
          padding: 16px 0;
          margin-bottom: 0;
        }
      }
    }
  }
  .download-plan {
    font-size: 14px;
    color: rgba(255, 255, 255, 0.5);
    position: absolute;
    bottom: 87px;
    left: 178px;
    cursor: pointer;
    @media only screen and (max-width: 1025px) {
      position: relative;
      left: 0;
      bottom: 0;
      margin-top: 40px;
    }
  }
}
</style>
