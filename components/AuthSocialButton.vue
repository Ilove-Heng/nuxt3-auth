<template>
    <button
      type="button"
      class="inline-flex justify-center w-full px-4 py-2 text-gray-500 bg-white rounded-md shadow-sm ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus:outline-offset-0"
    >
      <Icon :name="icon" />
    </button>
  </template>
  
  <script setup lang="ts">
  interface AuthSocialButtonProps {
    icon: string;
  }
  const props = defineProps<AuthSocialButtonProps>();
  </script>
  
  <style scoped></style>