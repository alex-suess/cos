<script setup>
defineProps({
  text: {
    type: String,
    required: true
  }
})
</script>
<template>
    <h1 class="text-5xl text-red-800 text-center mb-16 mt-16 font-handwriting">
        {{text}}
    </h1>
</template>