# Sintaxis y expresiones de plantillas

Vue utiliza una sintaxis de plantilla conocida como **sintaxis de doble bigote** (en inglés suena mejor...). Ahora que nos hemos adentrado en el mundo de Vue, vamos a ver qué nos ofrece las sintaxis de plantillas de este framework.

Para empezar, dentro de las dobles llaves se admite sintaxis de JavaScript:

### [src/App.vue](./src/App.vue)

```diff
<template>
  <div id="app">
    <img alt="Lemoncode logo" src="./assets/logo_lemoncode.png">
-    <h1>{{ header }}</h1>
+    <h1>{{ header.toLocaleUpperCase() }}</h1>
    <input type="text" v-model="header">
  </div>
</template>
```

Podemos utilizar expresiones ternarias, funciones... cualquier sintaxis de una sola línea que pueda ser evaluada de una sola vez:

```html
  <h1>{{ header.length > 20 ? header : 'Ups' }}</h1>
  <h1>{{ header.split('').reverse().join('') }}</h1>
```

[Volver al índice](../README_ES.md/#agenda)
