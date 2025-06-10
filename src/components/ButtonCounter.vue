<script setup>
import { ref } from 'vue'
const emit = defineEmits(['click']);

const handleClick = () => {
  emit('click');
};

</script>

<template>
  <button @click="handleClick">Cliquez-moi</button>
 
</template>