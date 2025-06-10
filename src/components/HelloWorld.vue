<script setup>
import { ref } from 'vue'

defineProps({ message : String })
</script>

<template>
<p>Bonjour Monde!</p> <br>

<p>{{ message }}</p>

</template>

<style scoped>

</style>
