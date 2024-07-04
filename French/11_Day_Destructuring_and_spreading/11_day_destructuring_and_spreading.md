<div align="center">
  <h1> 30 Days Of JavaScript: Destructuring and Spreading</h1>
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

[<< Day 10](../10_Day_Sets_and_Maps/10_day_Sets_and_Maps.md) | [Day 12>>](../12_Day_Regular_expressions/12_day_regular_expressions.md)

![Day 11](../images/banners/day_1_11.png)

- [Day 11](#day-11)
  - [Destructuring and Spread](#destructuring-and-spread)
    - [Destructing Arrays](#destructing-arrays)
    - [Destructuring during iteration](#destructuring-during-iteration)
    - [Destructuring Object](#destructuring-object)
    - [Renaming during structuring](#renaming-during-structuring)
    - [Destructuring object parameters](#destructuring-object-parameters)
  - [Spread or Rest Operator](#spread-or-rest-operator)
    - [Spread operator to copy array](#spread-operator-to-copy-array)
    - [Spread operator to add item to an array](#spread-operator-to-add-item-to-an-array)
    - [Spread operator to combine arrays](#spread-operator-to-combine-arrays)
    - [Spread operator to spread array as arguments](#spread-operator-to-spread-array-as-arguments)
  - [💻 Exercises](#-exercises)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# Day 11

## Destructuring and Spread

La déstructuration est une fonctionnalité de JavaScript qui rend l'extraction de valeurs des tableaux ou des propriétés des objets plus facile. L'opérateur spread (`...`) permet de répartir les éléments d'un tableau ou les propriétés d'un objet.

### Destructing Arrays

Nous pouvons déstructurer les éléments d'un tableau de la manière suivante :

```js
const numbers = [1, 2, 3]
let [numOne, numTwo, numThree] = numbers

console.log(numOne, numTwo, numThree) // 1 2 3
```

### Destructuring during iteration

Nous pouvons également déstructurer les éléments d'un tableau lors de l'itération.

```js
const fullStack = [['HTML', 'CSS', 'JS', 'React'], ['Node', 'Express', 'MongoDB']]

for(const [first, second, third] of fullStack) {
  console.log(first, second, third)
}
```

### Destructuring Object

Nous pouvons déstructurer les propriétés d'un objet de la manière suivante :

```js
const rectangle = {
  width: 20,
  height: 10,
  area: 200
}
let { width, height, area } = rectangle

console.log(width, height, area) // 20 10 200
```

### Renaming during structuring

Nous pouvons renommer les variables lors de la déstructuration.

```js
const rectangle = {
  width: 20,
  height: 10,
  area: 200
}
let { width: w, height: h, area: a } = rectangle

console.log(w, h, a) // 20 10 200
```

### Destructuring object parameters

Nous pouvons également déstructurer les paramètres d'un objet dans une fonction.

```js
const calculatePerimeter = ({ width, height }) => {
  return 2 * (width + height)
}

console.log(calculatePerimeter(rectangle)) // 60
```

## Spread or Rest Operator

L'opérateur spread (`...`) permet de répartir les éléments d'un tableau ou les propriétés d'un objet.

### Spread operator to copy array

Nous pouvons copier un tableau en utilisant l'opérateur spread.

```js
const numbers = [1, 2, 3, 4, 5]
const numbersCopy = [...numbers]

console.log(numbersCopy)
```

### Spread operator to add item to an array

Nous pouvons ajouter des éléments à un tableau en utilisant l'opérateur spread.

```js
const numbers = [1, 2, 3, 4, 5]
const newNumbers = [...numbers, 6, 7, 8]

console.log(newNumbers)
```

### Spread operator to combine arrays

Nous pouvons combiner plusieurs tableaux en utilisant l'opérateur spread.

```js
const frontEnd = ['HTML', 'CSS', 'JS', 'React']
const backEnd = ['Node', 'Express', 'MongoDB']

const fullStack = [...frontEnd, ...backEnd]
console.log(fullStack)
```

### Spread operator to spread array as arguments

Nous pouvons répartir les éléments d'un tableau en tant qu'arguments de fonction en utilisant l'opérateur spread.

```js
const sum = (a, b, c) => a + b + c

const numbers = [1, 2, 3]

console.log(sum(...numbers))
```

## 💻 Exercises

### Exercises: Level 1

1. Déstructurez le tableau suivant : `const numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]`.
2. Déstructurez les propriétés de l'objet rectangle : `const rectangle = { width: 20, height: 10, area: 200 }`.

### Exercises: Level 2

1. Utilisez l'opérateur spread pour créer une copie du tableau `numbers`.
2. Utilisez l'opérateur spread pour combiner deux tableaux.

### Exercises: Level 3

1. Déstructurez les propriétés de l'objet `user` et renommez les variables : `const user = { name: 'Asabeneh', title: 'Programmer', country: 'Finland' }`.
2. Utilisez l'opérateur spread pour ajouter de nouveaux éléments à un tableau.