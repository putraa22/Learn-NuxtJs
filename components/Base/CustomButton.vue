<script setup>
const props = defineProps({
  disabled: { type: Boolean, default: false },
  gradient: { type: Boolean, default: false },
});
</script>

<template>
  <button
    :disabled="disabled"
    :class="`${
      gradient
        ? 'btn  border-none lg:text-base text-sm text-white bg-gradient-to-r from-[#D70F3A] via-[#FF3867] to-[#E20039] rounded-md w-full p-2  hover:shadow-md transition-all hover:scale-105 duration-300 hover:delay-150'
        : 'bg-blue-600 text-white rounded-md w-full p-2 lg:text-base text-sm hover:shadow-md transition-all hover:scale-105 duration-300 hover:delay-150'
    }`"
  >
    <slot />
  </button>
</template>
