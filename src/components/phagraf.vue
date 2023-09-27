<template>
  <div>
    <div class="relative">
      <div
          v-if="status"
          class="shadow-2xl shadow-black absolute mt-20 flex items-center justify-center flex-col left-0  w-full bg-white z-50 rounded-3xl">
        <div
            class="relative flex flex-col  w-full">
          <h3 class="pt-5 pb-5 ml-10">Şühedanın İzinde 500 Su Kuyusu Projesi</h3>
          <div class="h-full w-full absolute top-20"
               @click="closeWindow"
          >
            <div
                class="absolute top-[-50px] right-5 h-[25px] w-[25px]">
              <svg enable-background="new 0 0 24 24" height="24" viewBox="0 0 24 24" width="24" focusable="false"
                   style=" pointer-events: none; display: block; width: 100%; height: 100%; fill: white; ">
                <path
                    d="m12.71 12 8.15 8.15-.71.71L12 12.71l-8.15 8.15-.71-.71L11.29 12 3.15 3.85l.71-.71L12 11.29l8.15-8.15.71.71L12.71 12z"></path>
              </svg>
            </div>
          </div>
          <div
              class="flex ml-auto mr-auto  h-[85%] w-[85%] items-center">
            <div class="h-full w-full pb-10">
              <video class="h-full w-full flex items-center" controls
                     src="">
              </video>
            </div>
          </div>
        </div>
      </div>
      {{ status }}


      <div>
        <div class="flex flex-col gap-10 text-[80%] p-5 tablet:p-0 tablet:text-[100%]">
          <p>
            Yaklaşık bir asırdır meydana gelen savaş, doğal afet, çatışma, iklim değişikliği ve bunlara bağlı
            olarak sosyo-ekonomik
            krizlerin boyutu öylesine artmış ve değişmiştir ki, halihazırda insani yardım faaliyetlerine devam
            eden geleneksel
            kurumların geleneksel anlayış ve yöntemleri yetersiz kalmaya başlamıştır.
          </p>
          <p>
            İnsani yardım faaliyetlerinde insan sayısı fazlalaşmasına rağmen yardım fonları zamanla azalmakta ve
            bu nedenle
            sorunların çözümü her geçen gün biraz daha zorlaşmaktadır. Tek seferlik veya kısa vadeli çözümler
            dışında artık kalıcı
            çözümler üretilmesi zorunlu hale gelmiştir. İyilik Enerjinle Yayılsın projesi de bu kalıcı çözümler
            için ortaya çıkmış
            bir projedir.
          </p>
        </div>

        <div
            v-if="!status"
            class="relative flex justify-center mt-20"
             @click="openTheWindow">
          <img class="absolute z-[-1] opacity-[0.7] w-[110px] left-[50px] top-[-50px]" src="@/img/simsek.svg" alt="">
          <img class="absolute z-[-1] opacity-[0.7] w-[110px] right-[70px] bottom-[-50px]" src="@/img/yaprak.svg"
               alt="">
          <div
              class="flex absolute top-[40%] bg-[rgba(255,255,255,0.24)] hover:bg-[rgba(255,255,255,0.48)] h-[22%] items-center justify-center rounded-[100%] w-[9%] hover:border-2  hover:border-[#80BC00]">
            <img src="@/img/basla.svg" alt="">
          </div>
          <img class="w-[70%] rounded-2xl" src="@/img/resim.png" alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import {ref} from "vue";

const status = ref(false);

const openTheWindow = () => {
  status.value = !status.value
}

const closeWindow = () => {
  status.value = !status.value
}

</script>

<style lang="scss" scoped>

</style>
