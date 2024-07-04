<div align="center">
  <h1> 30 Days Of JavaScript: Promises</h1>
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

[<< Day 17](../17_Day_Web_storages/17_day_web_storages.md) | [Day 19>>](../19_Day_Closures/19_day_closures.md)

![Thirty Days Of JavaScript](../images/banners/day_1_18.png)

- [Day 18](#day-18)
  - [Promise](#promise)
  - [Callbacks](#callbacks)
    - [Promise constructor](#promise-constructor)
  - [Fetch API](#fetch-api)
  - [Async and Await](#async-and-await)
  - [💻 Exercises](#-exercises)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# Day 18

## Promise

Une `Promise` est un objet représentant l'achèvement ou l'échec éventuel d'une opération asynchrone. Une `Promise` peut être dans l'un des trois états suivants : `pending`, `fulfilled` ou `rejected`.

```js
const doSomething = new Promise((resolve, reject) => {
  if (true) {
    resolve('Success')
  } else {
    reject('Failure')
  }
})

doSomething
  .then(result => console.log(result)) // Success
  .catch(error => console.log(error))
```

## Callbacks

Les `callbacks` sont des fonctions passées en argument à une autre fonction, puis exécutées à l'intérieur de cette fonction.

```js
const doSomething = callback => {
  setTimeout(() => {
    const skills = ['HTML', 'CSS', 'JS']
    callback('It did not go well', skills)
  }, 2000)
}

const callback = (err, result) => {
  if (err) {
    return console.log(err)
  }
  return console.log(result)
}

doSomething(callback)
```

### Promise constructor

Le constructeur `Promise` est utilisé pour créer une nouvelle `Promise`. Il prend une fonction en argument avec deux paramètres : `resolve` et `reject`.

```js
const promise = new Promise((resolve, reject) => {
  const success = true
  if (success) {
    resolve('It succeeded')
  } else {
    reject('It failed')
  }
})

promise
  .then(result => console.log(result)) // It succeeded
  .catch(error => console.log(error))
```

## Fetch API

L'API `fetch` est une interface moderne permettant de faire des requêtes réseau. Elle remplace l'ancienne `XMLHttpRequest`.

```js
const url = 'https://jsonplaceholder.typicode.com/posts'

fetch(url)
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.log(error))
```

## Async and Await

`async` et `await` sont des fonctionnalités modernes de JavaScript qui facilitent la gestion du code asynchrone.

```js
const fetchData = async () => {
  try {
    const response = await fetch(url)
    const data = await response.json()
    console.log(data)
  } catch (error) {
    console.log(error)
  }
}

fetchData()
```

## 💻 Exercises

### Exercises: Level 1

1. Créez une `Promise` qui se résout après 2 secondes et renvoie une chaîne de caractères "Hello, World!".

### Exercises: Level 2

1. Utilisez `fetch` pour obtenir des données à partir de l'API `https://jsonplaceholder.typicode.com/users` et affichez les noms des utilisateurs.

### Exercises: Level 3

1. Utilisez `async` et `await` pour obtenir des données à partir de l'API `https://jsonplaceholder.typicode.com/users` et affichez les noms des utilisateurs.
2. Créez une fonction `postData` qui envoie des données à l'API `https://jsonplaceholder.typicode.com/posts` et affiche la réponse du serveur.