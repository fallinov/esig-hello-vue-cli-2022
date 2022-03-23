<template>
  <div>
    <h1>Produits</h1>
    <ul>
      <li>{{ nom }}</li>
      <li>{{ prenom }}</li>
    </ul>
    <BoutonMagique couleur="red" />
    <BoutonMagique couleur="yellow" />
    <BoutonMagique couleur="blue">Bonjour</BoutonMagique>
  </div>
</template>

<script>
/* @ représente le dossier src/ de l'app */
import BoutonMagique from "@/components/BoutonMagique";
export default {
  name: "ProduitsView",
  components: { BoutonMagique },
  data() {
    return {
      nom: "Fallet",
      prenom: "Steve",
    };
  },
};
</script>

<style lang="sass" scoped>
h1
  color: green
</style>
