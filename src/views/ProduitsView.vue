<template>
  <div>
    <h1>Produits</h1>
    <ul>
      <li>{{ nom }}</li>
      <li>{{ prenom }}</li>
    </ul>
    <BoutonMagique couleur="red">Bonjour</BoutonMagique>
    <BoutonMagique @coucou="bonjour">Adieu</BoutonMagique>
    <BoutonMagique couleur="blue" couleur-txt="red">Tcho</BoutonMagique>
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
  methods: {
    bonjour(txt) {
      this.nom = txt;
    },
  },
};
</script>

<style lang="sass" scoped>
h1
  color: green
</style>
