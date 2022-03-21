<template>
  <div id="fifth" class="main__right__fifth full-height">
    <div class="main__right__third main__right__fifth__item">
      <p><span class="title">КОММЕРЦИЯ</span></p>
      <h2 class="semibold">КОММЕРЦИЯ</h2>
      <h2>В КОМПЛЕКСЕ ТАЛИСМАН</h2>
      <p class="text1">
        На территории комплекса TALISMAN есть ко-<br />
        фейня, супермаркет, салон красоты, ресторан<br />
        и многое другое. Также в доступности распо-<br />
        ложены крупные строительные магазины,<br />
        дошкольные образовательные центры, архе-<br />
        ологический парк.
      </p>
    </div>
    <div class="main__right__fifth__item"></div>
    <div class="main__right__fifth__item"></div>
    <div class="main__right__fifth__item">
      <p class="text2">
        В жилом комплексе TALISMAN предусмотрен<br />
        просторный одноэтажный подземный паркинг–<br />
        благодаря этому внутренние дворы и терри-<br />
        тория комплекса не будут заставлены<br />
        машинами. Такое преимущество станет<br />
        немаловажным при выборе ЖК для семей,<br />
        где есть дети и пожилые родители,
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "FifthComponent",
};
</script>

<style lang="scss">
.main__right__fifth {
  padding: 0;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(2, 1fr);
  @media only screen and (max-width: 850px) {
    grid-template-columns: 1fr;
    grid-template-rows: repeat(4, 1fr);
    height: 100vh !important;
  }
  @media only screen and (max-width: 450px) {
    padding: 12px 0 0 !important;
  }

  &__item {
    color: #fff;
    @media only screen and (max-width: 850px) {
      padding: 12px 52px!important;
    }

    &:nth-child(2) {
      background: url("/06.jpg") no-repeat center center;
      background-size: cover;
    }

    &:nth-child(3) {
      background: url("/07.jpg") no-repeat center center;
      background-size: cover;
      @media only screen and (max-width: 850px) {
        order: 4;
      }
    }

    &:nth-child(4) {
      display: flex;
      justify-content: center;
      align-items: center;
    }

    &.main__right__third {
      background: none;
    }

    h2,
    p {
      text-align: left;
      letter-spacing: 1px;
    }

    h2 {
      font-size: 2vw;
      font-family: "FiraSans-Regular";
      margin-bottom: 1vw;
      @media only screen and (max-width: 850px) {
        font-size: 16px;
        margin-bottom: 12px;
      }
      &.semibold {
        font-family: "FiraSans-SemiBold";
        margin-bottom: 0;
        margin-top: 1.5vw;
        @media only screen and (max-width: 850px) {
          font-size: 16px;
        }
      }
    }

    p {
      font-family: "FiraSans-Regular";
      font-size: 0.8vw;
      line-height: 1.4vw;
      letter-spacing: 0.2 vwpx;
      &.text1, &.text2 {
        @media only screen and (max-width: 850px) {
          font-size: 10px;
          line-height: initial;
          font-weight: 300;
          margin-bottom: 12px;
        }
      }
      @media only screen and (max-width: 850px) {
        font-size: 14px;
      }
      span.title {
        @media only screen and (max-width: 850px) {
          font-size: 10px;
        }
      }
    }
  }
}
</style>
