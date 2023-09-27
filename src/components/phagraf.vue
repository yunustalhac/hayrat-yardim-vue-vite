<template>
  <div class="flex flex-col gap-10">
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
    <div>
      <video-fill :is="active" @eventEmit="closeWindow"/>
      <div
          @click="openWindowPage"
          class="relative flex justify-center met-20">
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
</template>

<script setup>
import VideoFill from "@/components/video-fill.vue";
import {ref} from "vue";

const active = ref(false)


const closeWindow = () => {
  active.value=false
}


const openWindowPage = () => {
  active.value = true
}
</script>

<style lang="scss" scoped>

</style>
