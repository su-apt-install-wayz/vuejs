# Projet Vite Vue TypeScript

Ce projet utilise Vite pour le développement rapide avec Vue.js et TypeScript. Il intègre Tailwind CSS, Bootstrap, et Vue Router pour la gestion de l'application.

## Installation

Suivez ces étapes pour installer et démarrer le projet localement :


### 1. Création du projet

```sh
npm create @vite-pwa/pwa@latest vue-app -- --template vue-ts
```
```sh
cd vue-app
```


### 2. Installation des dépendances

```sh
npm install
npm install vue-router@4
npm install tailwindcss @tailwindcss/vite
npm install bootstrap @popperjs/core
npm install bootstrap@5.3.3
```


### 3. Configuration du projet

Dossier Plugins : Créer un dossier plugins pour les extensions personnalisées.

Fichier Router : Créer router.ts dans plugins pour configurer Vue Router.

```ts
import { createRouter, createWebHistory } from "vue-router";
import Home from "../views/Home.vue";
import Login from "../views/Login.vue";

const routes = [
  {path: '/', name: 'Home', component: Home},
  {path: '/login', name: 'Login', component: Login},
];

const router = createRouter({
    routes,
    history: createWebHistory(),
});

export default router;
```

Modifier le fichier App.vue

```ts
<template>
  <router-view />
</template>

<script setup>
import { RouterView } from 'vue-router';
</script>
```

Pages : Créer Home.vue et Login.vue dans le dossier views.


### 4. Configuration de Tailwind CSS

Ajoutez Tailwind CSS à votre projet. Assurez-vous que votre fichier vite.config.ts contient la configuration nécessaire.

```ts
import tailwindcss from '@tailwindcss/vite'
```
```ts
plugins: [vue(), tailwindcss(), VitePWA({
```
Ajoutez la ligne dans le fichier style.css de ```.src/```

```css
@import "tailwindcss";
```


### Démarrage du serveur de développement

Pour démarrer l'application en mode développement, utilisez la commande suivante :

```sh
npm run dev
```


### Structure du projet

```lua
vue-app/
├── src/
│   ├── components/
│   ├── views/
│   │   ├── Home.vue
│   │   ├── Login.vue
│   ├── plugins/
│   │   ├── router.js
│   ├── main.ts
│   ├── App.vue
├── vite.config.ts
├── tailwind.config.js
└── package.json
```
