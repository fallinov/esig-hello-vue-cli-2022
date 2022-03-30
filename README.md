# Démo Vue CLI
* Guide Vue CLI : https://cli.vuejs.org/guide/installation.html
* Doc Vue 2 en FR : https://fr.vuejs.org/v2/guide/index.html
## Commandes de base
### Initialiser le projet 
Télécharge les paquets, librairies avec NPM
```
npm install
```

### Démarre le serveur de développement
Le mode **Hot reload** est activé
=> Recharge la page automatiquement à chaque sauvegarde `(CTRL + S)`
```
npm run serve
```

### Création de la version de production
Compile et minimize, optimize les fichiers pour la production.

Le résultat est disponible dans le dossier `dist/`.
```
npm run build
```

### Analyse vos fichiers avec JS Lint  
Corrige automatiquement certaines erreurs et affiche les corrections nécessaires.
```
npm run lint
```
## Objectifs deu 30.3.2022

### Liaisons de classes et de styles
``` html
<div
  class="static"
  :class="{ active: isActive, 'text-danger': hasError }"
></div>
```
``` javascript
data: {
  isActive: true,
  hasError: false
}
```
``` html
<div class="static active"></div>
```

### Communiquer entre composants 
#### Avec des props 
Du composant parent aux enfants
``` javascript
export default {
  name: "MonBouton",
  props: ['couleurTexte', 'couleurFond'],
};
```
Utilisation des props comme des attributs dans le composant.
``` html
<mon-bouton couleur="couleur-texte" couleur-fond="vert"></div>
```

Les noms d’**attributs HTML sont insensibles à la casse**, aussi les navigateurs interprèteront de
la même manière les majuscules et les minuscules.

Il faut donc utiliser le **kebab-case** pour écrire les props dans le HTML.

#### Avec des événemements personalisés 
Du composant enfant à son parent

Émettre un événement
``` javascript
this.$emit('coucou')
```
Écouter un composant
``` html
<mon-composant @coucou="alert('Coucou !')" />
```
