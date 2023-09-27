<template>
  <section>
    <img class="absolute logo" src="@/img/title-icon.png">
    <div class="h-full">
      <div class="absolute h-[100vh]  w-full top-0 left-0">
        <img class=" h-full w-full" src="@/img/arkaplan.png">
      </div>
      <div>
        <img class="laptop:w-[110px] laptop>:top-[25px] laptop>:left-[20px] laptop:h-[39px] absolute h-[42px] w-[125px] left-[10px] top-[10px] tablet:top-[25px] tablet:left-[20px] tablet:w-[190px] tablet:h-[64px]" src="../img/Logo.png">
        <div>
          <div>
            <img class="title h-[85vh] w-[80%] ml-auto mr-auto" src="../img/title.svg">
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>

</script>


<style scoped>
@keyframes fade-in {
  0% {
    opacity: 0;
  }

  50%{
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}

@keyframes logo-spin {
  0% {
    opacity: 1;
  }
  100% {
    opacity: 0;
  }
}

.logo {
  opacity: 0;
  animation: logo-spin 2s;
}

.title {
  animation: fade-in 2s;
}


</style>