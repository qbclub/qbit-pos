<script setup>

import data from '../data/store.json'
import logo from '../assets/logo.svg'


</script>
<template>

    <div class="d-flex justify-space-between ">
        <img src="../assets/logo.png" class="logo" />
        <div class="d-flex justify-center flex-column font-weight-bold">
            <div class="text-center" style="font-size:20px">
                <a href="tel:+73414150666"><v-icon icon="mdi-phone"></v-icon> 5-06-66</a>
            </div>
            <!-- <div class="text-center">пн-птн</div>
            <div> с 9.00 до 17.00</div> -->
        </div>
        <v-space></v-space>
    </div>
    <template>

        <v-carousel :continuous="false" :show-arrows="false" delimiter-icon="mdi-square" height="250"
            hide-delimiter-background cycle class="carousel">
            <v-carousel-item>
                <v-sheet height="100%" tile>
                    <div class="d-flex flex-column fill-height justify-center align-center">
                        <h1>
                            Скидка 5%
                        </h1>
                        <h1>на первый заказ</h1>
                    </div>
                </v-sheet>

            </v-carousel-item>
            <v-carousel-item>
                <v-sheet height="100%" tile>
                    <div class="d-flex fill-height justify-center align-center">
                        <div>
                           <img src="https://pos-center.ru/img/products/m/poscenter/ri-te-iyl-02f-lan-usb-dya_28.jpg" style="height: 200px;" alt="">

                        </div>
                        <div>
                            <h2 class="text-center">Фискальный регистратор</h2>
                            <h2 class="text-center">РИТЕЙЛ-02Ф</h2>
                            <h1 class="text-center">22000 руб.</h1>
                        </div>
                        
                    </div>
                </v-sheet>

            </v-carousel-item>
            <v-carousel-item>
                <v-sheet height="100%" tile>
                    <div class="d-flex fill-height justify-center align-center">
                        <div>
                           <img src="https://pos-center.ru/img/products/m/poscenter/hh-2d2-hd_28.jpg" style="height: 200px;" alt="">

                        </div>
                        <div>
                            <h2 class="text-center">Сканер штрихкода</h2>
                            <h2 class="text-center">POScenter HH 2D2 HD</h2>
                            <h1 class="text-center">3591 руб.</h1>
                        </div>
                    </div>
                </v-sheet>

            </v-carousel-item>
            <v-carousel-item>
                <v-sheet height="100%" tile>
                    <div class="d-flex fill-height justify-center align-center">
                        <div>
                           <img src="https://pos-center.ru/img/products/m/idata/i3_28.jpg" style="height: 200px;" alt="">

                        </div>
                        <div>
                            <h2 class="text-center">ТСД "i3"</h2>
                            <h1 class="text-center">29030 руб.</h1>
                        </div>
                    </div>
                </v-sheet>

            </v-carousel-item>
        </v-carousel>

    </template>
    <v-expansion-panels>

        <v-expansion-panel v-for="item, key in data">
            <v-expansion-panel-title class="font-weight-bold" style="font-size:20px">
                {{ item.groupName }}
            </v-expansion-panel-title>
            <v-expansion-panel-text>
                <v-row class="justify-center align-center">
                    <v-col cols="12" sm="6"  md="4" v-for="product in item.items">
                        <v-card  class="pa-2 w-100">
                            <h4 class="text-center">
                                {{ product.name }}
                            </h4>
                            <div class="d-flex">
                                <img :src="product.image" alt="" class="product-img">
                                <div class="d-flex justify-center align-center w-100"> <b style="font-size:20px">{{
            `${product.price} руб.` }}</b></div>
                            </div>

                            <div style="font-size:12px; opacity: 0.7;">
                                <div v-for="value, key in product.values">
                                    {{ `${key} : ${value}` }}
                                </div>

                            </div>

                        </v-card>
                    </v-col>
                </v-row>


            </v-expansion-panel-text>
        </v-expansion-panel>
    </v-expansion-panels>
    <v-divider color="black"></v-divider>
    <v-footer class="mt-16 text-center d-flex flex-column">
     

        <div class="pt-0 d-flex align-center justify-space-between w-100">
            <div>
                <div> <b>Официальный партнер</b> </div>
                <div> <a href="https://pos-center.ru/" target="_blank"><img src="../assets/logopos.png" alt="" class="logopos"></a>  </div>
              
            </div>
            <div >
                <div> <b>ИП Грачев А.В.</b> </div>
                <div> <b>ИНН 182900345213</b> </div>
                <div> <b>г. Глазов</b> </div>
            </div>
           
        </div>

        <v-divider></v-divider>

        <div>
           <a href="https://qbit-club.com/" target="_blank">Сделано в Кубит</a> 
        </div>
    </v-footer>
</template>
<style scoped>
.logo, .product-img {
    max-height: 80px;
}

.logopos {
    max-height: 40px;
}
 h1{
    font-size: clamp(1.125rem, 0.0313rem + 3.5vw, 2rem);
}
h2{
    font-size: clamp(1rem, 0.0625rem + 3vw, 1.75rem);
}
</style>