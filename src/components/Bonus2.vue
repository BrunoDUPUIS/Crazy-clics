<script setup>
const colorsList = [
  'bleu',
  'vert',
  'rose',
  'orange',
  'violet',
  'marron',
  'jaune',
  'noir',
  'rouge',
  'gris',
]
const randomColor = () => {
  const randomNumber = Math.floor(Math.random() * colorsList.length)
  alert(colorsList[randomNumber])
}
</script>
<template>
  <section>
    <button @click="randomColor()">Couleur surprise</button>
  </section>
</template>
<style scoped>
section {
  display: flex;
  justify-content: center;
}
button {
  margin-top: 20px;
  border: 2px solid #791e75;
  color: #791e75;
  font-size: 32px;
  border-radius: 25px;
  padding: 0 15px;
  background-color: white;
}
</style>
