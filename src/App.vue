<script setup>
// 
import { ref } from 'vue'
// Ici je suis en javascript
// En vanilla 
// J'attrappe l'element du dom et je modifie son contenu
const title = "Alex's compteur"
// Dans le hmtl j'attrappe l'element du dom et je lui assigne une variable {title}
const compteur = ref(0);
const compteurColor = ref('green');

const increment = () => {
  compteur.value++
}
const decrement = () => {
  if (compteur.value > 0) {
    compteur.value--
  }

}
// 1 dans le noeud html directement > double moustache
// 2 
</script>

<template>
  <span class="counter-title" >{{ title }}</span>
  <div class='container'>
    <!-- :style="{color: compteur == 0 ? 'crimson' : 'green'}" -->
    <!-- :class="{positive: compteur > 0, zero: compteur == 0}" -->
    <div class='counter-container'>
      <span class="counter-display" :class="{'zero': compteur == 0}">{{ compteur }}</span>
    </div>

    <div class='buttons-container'>
      <button id='moins' @click="decrement" >-</button>
      <button id='plus' @click="increment">+</button>
    </div>
  </div>
</template>

<style scoped>
.positive{
  color:green; 
}
.zero{
  color:crimson
}
</style>
