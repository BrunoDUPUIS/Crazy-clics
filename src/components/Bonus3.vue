<script setup>
const colorsList = [
  { name: 'bleu', hexa: '#0B71BA' },
  { name: 'vert', hexa: '#39B639' },
  { name: 'orange', hexa: '#EA8512' },
  { name: 'violet', hexa: '#721D7D' },
  { name: 'marron', hexa: '#713928' },
  { name: 'jaune', hexa: '#DED94B' },
  { name: 'noir', hexa: '#1C1C18' },
  { name: 'rouge', hexa: '#F11919' },
  { name: 'gris', hexa: '#9C9696' },
]
const randomColorBis = () => {
  const randomNumber = Math.floor(Math.random() * colorsList.length)
  alert(
    `Vous obtenez du ${colorsList[randomNumber].name} dont le code hexadécimal est ${colorsList[randomNumber].hexa}. `,
  )
}
</script>
<template>
  <section>
    <div>
      <button @click="randomColorBis()">Couleur surprise version bis</button>
    </div>
  </section>
</template>
<style scoped>
section {
  display: flex;
  justify-content: center;
}
button {
  border: 2px solid;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 26px;
  background-color: white;
  border: none;
  height: 46px;
  width: 396px;
}
div {
  height: 50px;
  width: 400px;
  /* border: 1px solid red; */
  background: linear-gradient(to right, red, orange, yellow, green, blue);
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
