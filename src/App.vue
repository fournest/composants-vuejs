<script setup>
import HelloWorld from './components/HelloWorld.vue'
import ButtonCounter from './components/ButtonCounter.vue'
import Card from './components/Card.vue'
import Home from './components/Home.vue';
import About from './components/About.vue';
import Contact from './components/Contact.vue';
import { ref, shallowRef } from 'vue'

const counter = ref(0);
function increment() {
  counter.value++
}

const componentName = shallowRef(Home);

</script>

<template>
  <HelloWorld message="Bienvenue !!!" /> <br>
  <ButtonCounter @click="increment" />
  <p class="counter">{{ counter }}</p><br>
  <Card>
    <template #header>
      <h1> UN TITRE!</h1>
    </template>
    <main>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam expedita perspiciatis beatae alias quia
        tempore
        nisi molestiae. Quod soluta esse odio odit dignissimos. Nam, inventore?</p>
    </main>

    <template #footer>
      <p> Ceci est un footer!!</p>
    </template>


  </Card>

  <div id="app">
    <h2>Application de Composants Dynamiques</h2>
    <br>
    <nav>
      <button @click="componentName = Home">Accueil</button>
      <button @click="componentName = About">À propos</button>
      <button @click="componentName = Contact">Contact</button>
    </nav>
    <br>
    <main>
      <component :is="componentName"></component>
    </main>
  </div>





</template>



<style scoped>

#app {
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
nav {
  display: flex;
  margin-bottom: 30px;
}

nav button {
  background-color: #42b983;
  color: white;
  border: none;
  padding: 10px 20px;
  margin: 0 10px;
  border-radius: 5px;
  cursor: pointer;
  font-size: 16px;
  transition: background-color 0.3s ease;
}

nav button:hover {
  background-color: #368a68;
}

main {
  border: 1px solid #ddd;
  padding: 20px;
  border-radius: 10px;
  max-width: 800px;
  margin: 0 auto;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}
</style>