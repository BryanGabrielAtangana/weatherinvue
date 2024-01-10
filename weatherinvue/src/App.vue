<template>
  <div class="w-full min-h-screen bg-violet-300">
    <SiteNavigation />
    <RouterView />
  </div>
</template>

<script setup>
import SiteNavigation from "./components/SiteNavigation.vue";
import { RouterView } from "vue-router";
</script>

<style lang="scss" scoped></style>
