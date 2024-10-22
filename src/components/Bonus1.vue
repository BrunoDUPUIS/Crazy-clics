<script setup>
const word1 = 'aLigaTOR'
const word2 = 'CHAMOIS'
const word3 = 'ElEpHaNt'
const word4 = 'wombaT'
// const correctTheWord = word => {
//   const wordCorrect = word[0].toUpperCase() + word.slice(1, 8).toLowerCase()
//   alert(wordCorrect)
// }
/* autre possibilité de faire, avec une boucle */

const correctTheWord = word => {
  let str = ''

  for (let i = 0; i < word.length; i++) {
    if (i === 0) {
      str = str + word[i].toUpperCase()
    } else {
      str = str + word[i].toLowerCase()
    }
  }
  alert(str)
}
</script>
<template>
  <section>
    <button @click="correctTheWord(word1)">{{ word1 }}</button>
    <button @click="correctTheWord(word2)">{{ word2 }}</button>
    <button @click="correctTheWord(word3)">{{ word3 }}</button>
    <button @click="correctTheWord(word4)">{{ word4 }}</button>
  </section>
</template>
<style scoped>
section {
  display: flex;
  justify-content: space-around;
}
button {
  background-color: #60e6b4;
  border: none;
  border-radius: 5px;
  padding: 5px 10px;
  margin-top: 20px;
}
</style>
