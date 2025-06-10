<script setup>
import { ref } from 'vue'

</script>

<template>
    <div class="card">
        <header>
            <slot name="header"></slot>
        </header>
        <main>
            <slot></slot>
        </main>
        <footer>
            <slot name="footer"></slot>
        </footer>
        
    </div>

</template>

<style scoped>
.card {
    border: 2px solid royalblue;
    background-color: lightsalmon;
    padding: 25px;
    border-radius: 25px;
}

header {
    text-align: center;
    color: cyan;
    background-color: magenta;
    border-radius: 10px;
}

footer {

    text-align: center;
    font-size: 25px;
    font-family:fantasy;
    color: blueviolet;
    background-color: cadetblue;
    border-radius: 25px;
}
</style>