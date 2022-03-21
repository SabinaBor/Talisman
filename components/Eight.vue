<template>
  <div id="eight" class="main__right__third main__right__eight full-height">
    <div>
      <p><span class="title">ИНФРАСТРУКТУРА</span></p>
      <p>
        <strong>ГЕНЕРАЛЬНЫЙ ПЛАН</strong> КОМПЛЕКСА СО ВСТРОЕННЫМИ<br />
        ПОМЕЩЕНИЯМИ И ПАРКИНГОМ
      </p>
    </div>
    <div class="main__right__eight__image">
      <img src="/05.jpg" />
    </div>
  </div>
</template>

<script>
export default {
  name: "EightthComponent",
};
</script>

<style lang="scss">
.main__right__eight {
  background: #dedede;
  padding: 40px 0 0 !important;
  display: grid;
  grid-template-rows: 136px 1fr;
  overflow-y: hidden;
  @media only screen and (max-width: 850px) {
    display: block;
    padding: 12px 0 0 !important;
    background: linear-gradient(-58.06deg, #e8eef8 0%, #fefefe 100%)!important;
  }
  & > div:first-child {
    @media only screen and (max-width: 850px) {
      padding: 0 52px;
      margin-bottom: 12px;
    }
  }

  & > div > p {
    padding-left: 8vw;
    margin-bottom: 0.8vw !important;
    span.title {
      color: #c2a582;
      @media only screen and (max-width: 850px) {
        font-size: 12px;
      }
    }
    &:nth-child(2) {
      margin-bottom: 0;
      color: #5f4526;
      font-size: 14px;
      @media only screen and (max-width: 850px) {
        font-size: 10px;
        margin-bottom: 10px;
      }
    }
  }
  &__image {
    overflow: hidden;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    @media only screen and (max-width: 850px) {
      max-height: 600px;
    }
    @media only screen and (max-width: 450px) {
      max-height: 300px;
    }
    img {
      width: 100%;
      margin-bottom: 136px;
      @media only screen and (max-width: 850px) {
        margin-bottom: 0;
      }
    }
  }
}
</style>
