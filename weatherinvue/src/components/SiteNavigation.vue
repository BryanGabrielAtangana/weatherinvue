<template>
  <header class="nav-container">
    <nav class="h-full flex flex-row justify-around items-center text-white">
      <RouterLink :to="{ name: 'home' }">
        <div class="common-flex">
          <i class="fa-solid fa-sun text-[1.5rem]"></i>
          <h1 class="font-Pacifico text-[1.5rem]">WeatherInVue</h1>
        </div>
      </RouterLink>
      <div>
        <i
          class="fa-solid fa-circle-info text-[1.5rem] cursor-pointer hover:text-violet-300 duration-150"
          @click="toggleModal"
        ></i>
      </div>
      <BaseModal :modalActive="modalActive" @close-modal="toggleModal"
        ><p class="text-gray-700">
          Hey hi little berry boy comming near our field
        </p></BaseModal
      >
    </nav>
  </header>
</template>

<script setup>
import { ref } from "vue";
import { RouterLink } from "vue-router";
import BaseModal from "./BaseModal.vue";

const modalActive = ref(null);
const toggleModal = () => {
  modalActive.value = !modalActive.value;
};
</script>

<style scoped>
.nav-container {
  @apply sticky w-full h-14 bg-violet-500 shadow-lg;
}
.common-flex {
  @apply flex flex-row  gap-2 justify-center items-center;
}
</style>
