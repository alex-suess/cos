<script setup>
defineProps({
  url: {
    type: String,
    required: true
  },
  text:{
    type: String,
    required: false
  }
})
</script>
<template>
    <div class="text-center">
    <a :href="url" target="_blank" class="bg-green-500 text-white p-4 rounded-md mb-8 inline-block"> {{text?text:"blubbzumbeispiel"}} </a>
    </div>
</template>