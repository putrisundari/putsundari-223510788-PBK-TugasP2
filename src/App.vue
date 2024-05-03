<template>
  <div>
  
    <p v-bind:class="titleclass">
      Tugas 2 Pratikum Pemrograman Berbasis Komponen
    </p>
    <h3 v-bind:class="titleclass">
    Putri Sundari [223510788] </h3> 

    <h1>Event Listeners</h1>
    <button @click="changeColor">Change Color</button>
    <div :style="{ backgroundColor: bgColor, padding: '10px' }">{{ message }}</div>
    
  </div>

</template>

<script setup>
import { ref, reactive } from 'vue'

const titleclass = ref("class")

const message = ref('click "change color" to change the random color!');
const bgColor = ref('#add8e6'); 

const changeColor = () => {
  bgColor.value = '#' + Math.floor(Math.random()*16777215).toString(16);
};
</script>

<style scoped>
.class {
  font-size: 22px;
  color: #000080(235, 232, 233);
  font-family: 'Times New Roman';
}
</style>
