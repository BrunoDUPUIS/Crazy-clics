<template>
  <section>
    <button v-on:click="console.log(`Hello World !`)">
      Affiche un message dans la console
    </button>
    <button @click="console.log(`Bienvenue au reacteur`)">
      Affiche un autre message dans la console
    </button>
  </section>
</template>
<style scoped>
section {
  display: flex;
  justify-content: center;
}
button {
  color: #c19a3a;
  border: 1px solid #c19a3a;
  border-radius: 10px;
  padding: 10px;
  background-color: white;
}
</style>
