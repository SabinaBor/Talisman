<template>
    <div id="eightth" class="main__right__ninth full-height">
        <div class="contacts">
            <div class="contacts__top">
                <h3>ЗАКАЖИТЕ ЗВОНОК!</h3>
                <p>Мы свяжемся с вами и ответим на все ваши вопросы</p>
                <div class="contacts__top__form">
                    <input type="text" v-model="name" placeholder="Имя" />
                    <input type="text" v-model="phone_number" placeholder="Номер телефона: +7" />
                    <button class="contacts__top__form__btn">
                        <img src="../assets/images/arrow-right_yellow.svg" alt="image" />
                    </button>
                </div>
            </div>
            <div class="contacts__middle">
                <div class="contacts__middle__left">
                    <p>
                        НАШИ КОНТАКТЫ
                    </p>
                    <p>
                        моб: +7 777 393 2222
                    </p>
                    <p>
                        тел: +7 724 393 2222
                    </p>
                    <p>
                        email: talisman@taraz.kz
                    </p>
                </div>
                <div class="contacts__middle__right">

                </div>
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
    name: "NinthComponent"
}
</script>

