<template>
  <header class="nav-container">
    <nav class="h-full flex flex-row justify-around items-center text-white">
      <div class="common-flex">
        <i class="fa-solid fa-sun text-[1.5rem]"></i>
        <h1 class="font-Pacifico text-[1.5rem]">WeatherInVue</h1>
      </div>
      <div><i class="fa-solid fa-circle-info text-[1.5rem]"></i></div>
    </nav>
  </header>
</template>

<script setup></script>

<style scoped>
.nav-container {
  @apply sticky w-full h-14 bg-violet-500 shadow-lg;
}
.common-flex {
  @apply flex flex-row  gap-2 justify-center items-center;
}
</style>
