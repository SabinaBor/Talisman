<template>
<div id="eight" class="main__right__third main__right__eight full-height">
    <div>
        <p><span class="title">ИНФРАСТРУКТУРА</span></p>
        <p><strong>ГЕНЕРАЛЬНЫЙ ПЛАН</strong> КОМПЛЕКСА СО ВСТРОЕННЫМИ<br />
        ПОМЕЩЕНИЯМИ И ПАРКИНГОМ</p>
    </div>
    <div class="main__right__eight__image">
        <img src="/04.png" />
    </div>
</div>
</template>

<script>
export default {
    name: "EightthComponent"
}
</script>

<style lang="scss">
.main__right__eight {
    background: #DEDEDE;
    padding: 40px 0 0!important;
    display: grid;
    grid-template-rows: 136px 1fr;
    overflow-y: hidden;
    
    &> div > p {
        padding-left: 8vw;
        margin-bottom: 0.8vw!important;
        span.title {
            color: #C2A582;
        }
        &:nth-child(2) {
            margin-bottom: 0;
            color: #5F4526;
            font-size: 1.2vw;
        }
    }
    &__image {
        display: flex;
        justify-content: center;
        img {
            width: 100%;
        }
    }
}
</style>
