<script setup>
/* partie 2 */
const displayName = () => {
  console.log("Je m'appelle Bruno")
}
const displayName2 = name => {
  alert(`je m'appelle ${name}`)
}
/* partie 3 */
const colors = {
  bleue: '#23b8d3',
  violette: '#a519a5',
  orange: '#ffa500',
  verte: '#44f178',
}
const displayColor = color => {
  alert(
    `Il s'agit de la couleur ${color} dont le code hexadécimal ${colors[color]}.`,
  )
}
/* partie 4 */
const displayRandomNumber = () => {
  const randomNumber = Math.floor(Math.random() * 100)
  alert(randomNumber)
}
/* partie 5 */

const convertToCm = km => {
  alert(`${km} kms, correspondent à ${km * 100000} cms`)
}
/* partie 6 */

const displayNetwork = brand => {
  alert(`Il s'agit du réseau ${brand}.`)
}
</script>

<template>
  <main>
    <h1>Crazy Clics !</h1>
    <section id="part1">
      <button v-on:click="console.log(`Hello World !`)">
        Affiche un message dans la console
      </button>
      <button @click="console.log(`Bienvenue au reacteur`)">
        Affiche un autre message dans la console
      </button>
    </section>
    <section id="part2">
      <button v-on:click="displayName">Comment t'appelles tu ?</button>
      <button @click="displayName2(`Bruno`)">Comment t'appelles tu ?</button>
    </section>
    <section id="part3">
      <h2>De quelle couleur s'agit-il ?</h2>
      <div id="color">
        <div
          @click="displayColor('bleue')"
          :style="{ backgroundColor: colors.bleue }"
        ></div>
        <div
          @click="displayColor('violette')"
          :style="{ backgroundColor: colors.violette }"
        ></div>
        <div
          @click="displayColor('orange')"
          :style="{ backgroundColor: colors.orange }"
        ></div>
        <div
          @click="displayColor('verte')"
          :style="{ backgroundColor: colors.verte }"
        ></div>
      </div>
    </section>
    <section id="part4">
      <h2>Le chiffre surprise</h2>
      <div><button @click="displayRandomNumber">Chiffre surprise</button></div>
    </section>
    <section id="part5">
      <div>
        <h2>Convertir des kms en cm :</h2>
        <div>
          <div @click="convertToCm(10)">10 kms</div>
          <div @click="convertToCm(50)">50 kms</div>
          <div @click="convertToCm(145)">145 kms</div>
          <div @click="convertToCm(459)">459 kms</div>
          <div @click="convertToCm(1579)">1579 kms</div>
          <div @click="convertToCm(3979)">3979 kms</div>
          <div @click="convertToCm(5000)">5000 kms</div>
          <div @click="convertToCm(7846)">7846 kms</div>
          <div @click="convertToCm(10979)">10979 kms</div>
        </div>
      </div>
    </section>
    <section id="part6">
      <font-awesome-icon
        :icon="['fab', 'github']"
        @click="displayNetwork('Github')"
      />
      <font-awesome-icon
        :icon="['fab', 'linkedin']"
        @click="displayNetwork('Linkedin')"
      />
      <font-awesome-icon
        :icon="['fab', 'instagram']"
        @click="displayNetwork('Instagram')"
      />
    </section>
  </main>
</template>

<style scoped>
section {
  margin-bottom: 30px;
  gap: 20px;
}
/* partie 1 */
#part1 {
  display: flex;
  justify-content: center;
}
#part1 > button {
  color: #c19a3a;
  border: 1px solid #c19a3a;
  border-radius: 10px;
  padding: 10px;
  background-color: white;
}
/* partie 2 */
#part2 {
  display: flex;
  justify-content: space-around;
}
#part2 > button {
  color: white;
  border: none;
  border-radius: 30px;
  padding: 10px;
  background: linear-gradient(10deg, #92cbcf, #8180d0);
}

/* partie 3 */
#color {
  display: flex;
  justify-content: center;
  gap: 20px;
}
#color > div {
  width: 60px;
  height: 60px;
  /* border: 1px solid red; */
  border-radius: 30px 0 30px 0px;
}
#part3 h2 {
  text-align: center;
  margin-bottom: 30px;
}
/* partie 4 */
#part4 > div {
  display: flex;
  justify-content: center;
}
#part4 > div > button {
  border: thick double pink;
  border-radius: 50%;
  width: 100px;
  height: 100px;
  background-color: #fc7f50;
  color: white;
}
#part4 h2 {
  text-align: center;
  margin-bottom: 30px;
}
/* partie 5 */
#part5 {
  display: flex;
  justify-content: center;
}
#part5 h2 {
  margin-bottom: 20px;
  text-align: center;
  color: #7624d6;
}
#part5 > div {
  /* border: 3px solid red; */
  height: 300px;
  width: 500px;
  background-color: #97fadf;
  padding: 10px;
  border-radius: 5px;
}
#part5 > div > div {
  /* border: 1px solid green; */
  height: 250px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 10px;
}
#part5 > div > div > div {
  border: 2px solid #7624d6;
  border-radius: 5px;
  width: calc((100% - 40px) / 3);
  display: flex;
  justify-content: center;
  align-items: center;
  color: #7624d6;
}
/* partie 6 */
#part6 {
  /* border: 1px solid red; */
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
}
#part6 > svg {
  margin: 20px;
  width: 50px;
  height: 50px;
}
</style>
