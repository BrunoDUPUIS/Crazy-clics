<script setup>
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
</script>
<template>
  <section>
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
</template>
<style scoped>
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
h2 {
  text-align: center;
  margin-bottom: 30px;
}
</style>
