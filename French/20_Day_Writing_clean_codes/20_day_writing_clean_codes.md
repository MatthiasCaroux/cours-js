<div align="center">
  <h1> 30 Days Of JavaScript: Writing Clean Codes</h1>
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

[<< Day 19](../19_Day_Closuers/19_day_closures.md) | [Day 21 >>](../21_Day_DOM/21_day_dom.md)

![Thirty Days Of JavaScript](../images/banners/day_1_20.png)
- [Day 20](#day-20)
  - [Writing clean code](#writing-clean-code)
    - [JavaScript Style Guide](#javascript-style-guide)
    - [Why we need style guide](#why-we-need-style-guide)
      - [Airbnb JavaScript Style Guide](#airbnb-javascript-style-guide)
      - [JavaScript Standard Style](#javascript-standard-style)
      - [Google JavaScript Style Guide](#google-javascript-style-guide)
  - [JavaScript Style Guides](#javascript-style-guides)
    - [Variables](#variables)
    - [Functions](#functions)
    - [Arrays](#arrays)
    - [Objects](#objects)
    - [Loops](#loops)
    - [Conditionals](#conditionals)
  - [💻 Exercises](#-exercises)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# Day 20

## Writing clean code

Écrire du code propre et maintenable est une compétence essentielle pour tout développeur. Cela permet de rendre le code plus lisible, compréhensible et facile à maintenir. Voici quelques guides de style et bonnes pratiques pour écrire du code JavaScript propre.

### JavaScript Style Guide

Un guide de style JavaScript est un ensemble de règles et de conventions sur la façon dont le code JavaScript doit être écrit et organisé.

### Why we need style guide

Les guides de style aident à maintenir la cohérence du code, facilitent la collaboration entre les développeurs et rendent le code plus lisible et compréhensible. Ils permettent également d'éviter les erreurs courantes et les mauvaises pratiques.

#### Airbnb JavaScript Style Guide

Le guide de style JavaScript d'Airbnb est l'un des guides de style les plus populaires et les plus utilisés. Il couvre un large éventail de règles et de bonnes pratiques pour écrire du code JavaScript propre et maintenable.

#### JavaScript Standard Style

Le JavaScript Standard Style est un guide de style JavaScript qui se concentre sur la simplicité et l'absence de configuration. Il n'a pas besoin de fichier de configuration et peut être utilisé directement.

#### Google JavaScript Style Guide

Le guide de style JavaScript de Google est un ensemble de conventions et de recommandations pour écrire du code JavaScript de haute qualité. Il est utilisé par les développeurs de Google et est également largement adopté par la communauté JavaScript.

## JavaScript Style Guides

### Variables

- Utilisez `const` pour les constantes et `let` pour les variables qui changent.
- Utilisez des noms de variables descriptifs et significatifs.
- Utilisez le camelCase pour nommer les variables.

```js
const firstName = 'John'
let age = 25
```

### Functions

- Utilisez des déclarations de fonctions ou des expressions de fonctions.
- Utilisez des noms de fonctions descriptifs et significatifs.
- Utilisez le camelCase pour nommer les fonctions.

```js
function calculateAge(birthYear) {
  return new Date().getFullYear() - birthYear
}

const getFullName = (firstName, lastName) => `${firstName} ${lastName}`
```

### Arrays

- Utilisez des méthodes de tableau intégrées pour manipuler les tableaux.
- Utilisez des noms de variables descriptifs et significatifs pour les tableaux.
- Utilisez le camelCase pour nommer les tableaux.

```js
const numbers = [1, 2, 3, 4, 5]
const fruits = ['apple', 'banana', 'orange']
```

### Objects

- Utilisez des objets pour regrouper des données liées.
- Utilisez des noms de variables descriptifs et significatifs pour les objets.
- Utilisez le camelCase pour nommer les objets.

```js
const person = {
  firstName: 'John',
  lastName: 'Doe',
  age: 25,
  getFullName() {
    return `${this.firstName} ${this.lastName}`
  }
}
```

### Loops

- Utilisez des boucles `for`, `while` ou des méthodes de tableau comme `forEach` pour itérer sur des tableaux.
- Utilisez des noms de variables descriptifs et significatifs pour les index de boucle.

```js
for (let i = 0; i < numbers.length; i++) {
  console.log(numbers[i])
}

numbers.forEach(number => console.log(number))
```

### Conditionals

- Utilisez des déclarations `if`, `else if` et `else` pour les conditions.
- Utilisez des opérateurs de comparaison appropriés.
- Utilisez des noms de variables descriptifs et significatifs pour les conditions.

```js
if (age >= 18) {
  console.log('You are an adult.')
} else if (age >= 13) {
  console.log('You are a teenager.')
} else {
  console.log('You are a child.')
}
```

## 💻 Exercises

### Exercises: Level 1

1. Déclarez des variables et assignez-leur des valeurs en utilisant les bonnes pratiques de nommage.
2. Écrivez une fonction qui calcule la somme de deux nombres en utilisant les bonnes pratiques de nommage.

### Exercises: Level 2

1. Créez un tableau de fruits et itérez dessus en utilisant une boucle `for` et une méthode de tableau.
2. Créez un objet `person` avec des propriétés et des méthodes, et utilisez-le pour afficher les informations de la personne.

### Exercises: Level 3

1. Écrivez une fonction qui prend un tableau de nombres et renvoie un nouveau tableau avec chaque nombre multiplié par 2.
2. Écrivez une fonction qui prend un objet `person` et ajoute une nouvelle propriété `isAdult` en fonction de l'âge de la personne.