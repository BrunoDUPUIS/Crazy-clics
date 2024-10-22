<script setup>
const displayName = () => {
  console.log("Je m'appelle Bruno")
}
const displayName2 = name => {
  alert(`je m'appelle ${name}`)
}
</script>
<template>
  <section>
    <button v-on:click="displayName">Comment t'appelles tu ?</button>
    <button @click="displayName2(`Bruno`)">Comment t'appelles tu ?</button>
  </section>
</template>
<style scoped>
section {
  display: flex;
  justify-content: space-around;
}
button {
  color: white;
  border: none;
  border-radius: 30px;
  padding: 10px;
  background: linear-gradient(10deg, #92cbcf, #8180d0);
}
</style>
