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
          <p class="white">ПЛОЩАДЬ: от 62 м^2</p>
          <p class="white">ЦЕНА: от 702 000 тг. за м^2</p>
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
          <p class="white">ПЛОЩАДЬ: от 75 м^2</p>
          <p class="white">ЦЕНА: от 650 000 тг. за м^2</p>
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
          <p class="white">ПЛОЩАДЬ: от 105 м^2</p>
          <p class="white">ЦЕНА: от 602 000 тг. за м^2</p>
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
  &__items {
    display: flex;
    margin: 0 auto;
    width: 100%;
    padding: 80px 70px;
    flex-wrap: wrap;
    justify-content: center;
  }
  &__item {
    width: calc(100% / 3 - 70px);
    &__top {
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
    }
  }
}
</style>
