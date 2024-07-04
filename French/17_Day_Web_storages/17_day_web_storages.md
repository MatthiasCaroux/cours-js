<div align="center">
  <h1> 30 Days Of JavaScript: Web Storages</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/asabeneh/">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>
  <a class="header-badge" target="_blank" href="https://twitter.com/Asabeneh">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/asabeneh?style=social">
  </a>

<sub>Author:
<a href="https://www.linkedin.com/in/asabeneh/" target="_blank">Asabeneh Yetayeh</a><br>
<small> January, 2020</small>
</sub>

</div>

[<< Day 16](../16_Day_JSON/16_day_json.md) | [Day 18 >>](../18_Day_Promises/18_day_promises.md)

![Thirty Days Of JavaScript](../images/banners/day_1_17.png)

- [Day 17](#day-17)
  - [HTML5 Web Storage](#html5-web-storage)
    - [sessionStorage](#sessionstorage)
    - [localStorage](#localstorage)
    - [Use case of Web Storages](#use-case-of-web-storages)
  - [HTML5 Web Storage Objects](#html5-web-storage-objects)
    - [Setting item to localStorage](#setting-item-to-localstorage)
    - [Getting item from localStorage](#getting-item-from-localstorage)
    - [Clearing the localStorage](#clearing-the-localstorage)
  - [💻 Exercises](#-exercises)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# Day 17

## HTML5 Web Storage

Le stockage Web HTML5 fournit deux mécanismes pour stocker des données côté client : `localStorage` et `sessionStorage`. Ces deux objets permettent de stocker des paires clé-valeur, mais avec des comportements différents.

### sessionStorage

`sessionStorage` est utilisé pour stocker des données pour la durée d'une session de page. Les données sont supprimées lorsque l'utilisateur ferme l'onglet ou le navigateur.

### localStorage

`localStorage` est utilisé pour stocker des données sans date d'expiration. Les données ne sont pas supprimées lorsque l'utilisateur ferme l'onglet ou le navigateur, et sont disponibles lors des visites ultérieures de la page.

### Use case of Web Storages

Les stockages Web peuvent être utilisés pour stocker des informations utilisateur, des paramètres de l'application, des jetons d'authentification, des paniers d'achat, etc.

## HTML5 Web Storage Objects

### Setting item to localStorage

Nous pouvons stocker des données dans `localStorage` en utilisant la méthode `setItem`.

```js
localStorage.setItem('firstName', 'Asabeneh')
localStorage.setItem('age', 250)
```

### Getting item from localStorage

Nous pouvons récupérer des données de `localStorage` en utilisant la méthode `getItem`.

```js
let firstName = localStorage.getItem('firstName')
let age = localStorage.getItem('age')
console.log(firstName, age)
```

### Clearing the localStorage

Nous pouvons supprimer un élément spécifique de `localStorage` en utilisant la méthode `removeItem` ou effacer tout le stockage en utilisant la méthode `clear`.

```js
localStorage.removeItem('firstName')
localStorage.clear()
```

## 💻 Exercises

### Exercises: Level 1

1. Stockez votre prénom, votre nom et votre âge dans le `localStorage`.
2. Récupérez votre prénom, votre nom et votre âge du `localStorage`.

### Exercises: Level 2

1. Stockez un objet utilisateur dans le `localStorage`.
2. Récupérez l'objet utilisateur du `localStorage`.

### Exercises: Level 3

1. Créez une application de liste de tâches qui permet aux utilisateurs de stocker leurs tâches dans le `localStorage`.
2. Ajoutez une fonctionnalité pour supprimer une tâche spécifique du `localStorage`.