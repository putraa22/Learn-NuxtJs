<script setup lang="ts">
const props = defineProps({
  types: {
    type: String,
    default: "text",
  },
  placeholder: {
    type: String,
    default: "Email",
  },
});
</script>
<template>
  <div>
    <input
      :type="types"
      :placeholder="placeholder"
      class="border border-gray-400 focus:outline-none outline-none rounded-md lg:p-2 p-1 lg:text-base text-sm w-full"
    />
  </div>
</template>
