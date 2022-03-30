<template>
  <button
    :style="'background-color:' + couleur + '; color:' + couleurTxt"
    :class="{ actif: actif }"
    @click="$emit('coucou', 'Pauline')"
  >
    <slot>Magique</slot>
  </button>
</template>

<script>
export default {
  name: "BoutonMagique",
  props: ["couleur", "couleurTxt"],
  data() {
    return {
      actif: true,
    };
  },
};
</script>

<style scoped>
button {
  background-color: green;
  color: white;
  font-weight: bold;
  border-radius: 10px;
  padding: 2px 4px;
}

button.actif {
  border: 4px solid black;
}
</style>
