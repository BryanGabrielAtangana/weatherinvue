<template>
  <div
    v-show="modalActive"
    class="absolute w-full h-screen bg-violet-950 bg-opacity-50 top-0 left-0 flex justify-center px-8"
  >
    <div
      v-if="modalActive"
      class="bg-white p-4 self-start mt-32 max-w-screen-md rounded-sm flex flex-col font-Rubik"
    >
      <slot />
      <button
        class="text-white mt-8 bg-violet-500 py-2 px-6"
        @click="$emit('close-modal')"
      >
        close
      </button>
    </div>
  </div>
</template>

<script setup>
defineEmits(["close-modal"]);
defineProps({
  modalActive: {
    type: Boolean,
    default: false,
  },
});
</script>

<style lang="scss" scoped></style>
