<script setup>
const displayNetwork = brand => {
  alert(`Il s'agit du réseau ${brand}.`)
}
</script>
<template>
  <section>
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
</template>
<style scoped>
section {
  /* border: 1px solid red; */
  display: flex;
  justify-content: center;
  margin-top: 20px;
}
svg {
  font-size: 40px;
  margin-right: 20px;
}
</style>
