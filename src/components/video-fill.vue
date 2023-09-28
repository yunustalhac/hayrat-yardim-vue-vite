<!-- ModalComponent.vue -->
<template>

  <div class="modal-overlay absolute bg-red-600" v-if="is" @click="closeModal">
    <div class="modal-container relative" @click.stop>
      <!-- Modal içeriğini buraya ekleyin -->
      <div @click="closeModal" class="absolute right-5">
        <svg width="22" height="22" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" class="icon">
          <path
              d="M12 22C6.477 22 2 17.523 2 12S6.477 2 12 2s10 4.477 10 10-4.477 10-10 10zm0-2a8 8 0 100-16.001A8 8 0 0012 20zm0-9.414l2.828-2.829 1.415 1.415L13.414 12l2.829 2.828-1.415 1.415L12 13.414l-2.828 2.829-1.415-1.415L10.586 12 7.757 9.172l1.415-1.415L12 10.586z"
              fill="currentColor"></path>
        </svg>
      </div>
      <div class="modal-content flex flex-col gap-5">
        <small class="font-bold desktop:text-xl tablet:text-xl">Şühedanın İzinde 500 Su Kuyusu Projesi</small>
        <video controls loop src="@/img/video.mp4" class="w-[100%]"></video>
      </div>
    </div>
  </div>
</template>

<script setup>

const {is} = defineProps(["is"]);
const emit = defineEmits(["eventEmit"]); // Event adını burada belirtin

const closeModal = () => {
  emit("eventEmit"); // Emit işlemi burada gerçekleştirin
}
</script>

<style scoped>
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 999;
}

.modal-container {
  background-color: white;
  padding: 20px;
  width: 60%;
  border-radius: 5px;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.5);
}

.modal-content {
  max-height: 70vh; /* Modal içeriğinin en fazla bu kadar yüksek olmasını sağlar */
  overflow-y: auto; /* İçeriğin taşması durumunda kaydırma çubuğunu gösterir */
}

</style>
