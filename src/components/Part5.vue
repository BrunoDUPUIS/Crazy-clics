<script setup>
const convertToCm = km => {
  alert(`${km} kms, correspondent à ${km * 100000} cms`)
}
</script>
<template>
  <section>
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
</template>
<style scoped>
section {
  display: flex;
  justify-content: center;
}
h2 {
  margin-bottom: 20px;
  text-align: center;
  color: #7624d6;
}
section > div {
  /* border: 3px solid red; */
  height: 300px;
  width: 500px;

  background: #9ef3e3;
  padding: 10px;
  border-radius: 5px;
}
section > div > div {
  /* border: 1px solid green; */
  height: 250px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 10px;
}
section > div > div > div {
  border: 2px solid #7624d6;
  border-radius: 5px;
  width: calc((100% - 40px) / 3);
  display: flex;
  justify-content: center;
  align-items: center;
  color: #7624d6;
}
</style>
