<script setup>
const displayRandomNumber = () => {
  const randomNumber = Math.floor(Math.random() * 100)
  alert(randomNumber)
}
</script>
>
<template>
  <section>
    <h2>Le chiffre surprise</h2>
    <div><button @click="displayRandomNumber">Chiffre surprise</button></div>
  </section>
</template>
<style scoped>
div {
  display: flex;
  justify-content: center;
}
button {
  border: thick double pink;
  border-radius: 50%;
  width: 100px;
  height: 100px;
  background-color: #fc7f50;
  color: white;
}
h2 {
  text-align: center;
  margin-bottom: 30px;
}
</style>
