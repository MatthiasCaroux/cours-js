<div align="center">
  <h1> 30 Days Of JavaScript: Functions</h1>
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

[<< Day 6](../06_Day_Loops/06_day_loops.md) | [Day 8 >>](../08_Day_Objects/08_day_objects.md)

![Thirty Days Of JavaScript](../images/banners/day_1_7.png)

- [📔 Day 7](#-day-7)
  - [Functions](#functions)
    - [Function Declaration](#function-declaration)
    - [Function without a parameter and return](#function-without-a-parameter-and-return)
    - [Function returning value](#function-returning-value)
    - [Function with a parameter](#function-with-a-parameter)
    - [Function with two parameters](#function-with-two-parameters)
    - [Function with many parameters](#function-with-many-parameters)
  - [Function with unlimited number of parameters](#function-with-unlimited-number-of-parameters)
    - [Unlimited number of parameters in regular function](#unlimited-number-of-parameters-in-regular-function)
    - [Unlimited number of parameters in arrow function](#unlimited-number-of-parameters-in-arrow-function)
  - [Anonymous Function](#anonymous-function)
  - [Expression Function](#expression-function)
  - [Self Invoking Functions](#self-invoking-functions)
  - [Arrow Function](#arrow-function)
  - [Functions with default parameters](#functions-with-default-parameters)
  - [💻 Exercises](#-exercises)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# 📔 Day 7

## Functions

Une fonction est un bloc de code conçu pour effectuer une tâche particulière. Une fonction est exécutée lorsqu'elle est appelée (appelée invoquée). Pour utiliser une fonction, nous devons la définir quelque part dans le scope à partir duquel nous souhaitons l'appeler.

### Function Declaration

Pour déclarer une fonction, nous utilisons le mot-clé `function`, suivi par un nom, suivi par des parenthèses `()`.

```js
// déclaration d'une fonction sans paramètre
function functionName() {
  // code à exécuter
}
functionName() // appel de fonction
```

### Function without a parameter and return

```js
function square() {
  let num = 2
  let sq = num * num
  console.log(sq)
}

square() // 4
```

### Function returning value

```js
function addTwoNumbers() {
  let numOne = 10
  let numTwo = 20
  let sum = numOne + numTwo
  return sum
}

console.log(addTwoNumbers()) // 30
```

### Function with a parameter

```js
function functionName(parm1) {
  // code à exécuter
}
// l'appel de fonction
functionName(parm1)
```

```js
function areaOfCircle(r) {
  let area = Math.PI * r * r
  return area
}

console.log(areaOfCircle(10)) // 314.1592653589793
```

### Function with two parameters

```js
function sumTwoNumbers(numOne, numTwo) {
  let sum = numOne + numTwo
  return sum
}

console.log(sumTwoNumbers(10, 20)) // 30
```

### Function with many parameters

```js
// cette fonction prend des tableaux en paramètre et les fusionne ensemble
function arrayValues(arr) {
  let newArr = []
  for (let i = 0; i < arr.length; i++) {
    newArr.push(arr[i])
  }
  return newArr
}

const result = arrayValues([1, 2, 3, 4, 5])
console.log(result) // [1, 2, 3, 4, 5]
```

## Function with unlimited number of parameters

### Unlimited number of parameters in regular function

```js
function sumAllNums() {
  let sum = 0
  for (let i = 0; i < arguments.length; i++) {
    sum += arguments[i]
  }
  return sum
}

console.log(sumAllNums(1, 2, 3, 4, 5)) // 15
```

### Unlimited number of parameters in arrow function

```js
const sumAllNums = (...args) => {
  let sum = 0
  for (const num of args) {
    sum += num
  }
  return sum
}

console.log(sumAllNums(1, 2, 3, 4, 5)) // 15
```

## Anonymous Function

Les fonctions anonymes sont des fonctions sans nom.

```js
const anonymousFun = function() {
  console.log('Je suis une fonction anonyme')
}
```

## Expression Function

Les fonctions d'expression sont des fonctions anonymes. Après avoir été définies, elles peuvent être appelées par leur nom.

```js
const square = function(n) {
  return n * n
}

console.log(square(2)) // 4
```

## Self Invoking Functions

Les fonctions auto-invoquées sont des fonctions qui sont invoquées automatiquement après leur définition.

```js
(function(n) {
  console.log(n * n)
})(2) // 4
```

## Arrow Function

Les fonctions fléchées sont des fonctions anonymes. Elles sont courtes et propres à écrire.

```js
const changeToUpperCase = arr => {
  const newArr = []
  for (const element of arr) {
    newArr.push(element.toUpperCase())
  }
  return newArr
}

const countries = ['Finland', 'Sweden', 'Norway', 'Denmark', 'Iceland']
console.log(changeToUpperCase(countries)) // ["FINLAND", "SWEDEN", "NORWAY", "DENMARK", "ICELAND"]
```

## Functions with default parameters

Les fonctions avec des paramètres par défaut permettent de passer des valeurs par défaut dans les fonctions.

```js
function greetings(name = 'Peter') {
  let message = `${name}, bienvenue dans 30 Days Of JavaScript!`
  return message
}

console.log(greetings())
console.log(greetings('Asabeneh'))
```

## 💻 Exercises

### Exercises: Level 1

1. Déclarez une fonction fullName et imprimez votre nom complet.
2. Déclarez une fonction fullName et retournez votre nom complet.

### Exercises: Level 2

1. Déclarez une fonction sumTwoNumbers et retourne la somme de deux nombres.
2. Déclarez une fonction qui calcule l'aire d'un rectangle.

### Exercises: Level 3

1. Déclarez une fonction multiplyAllNums qui retourne le produit de tous les paramètres passés.
2. Déclarez une fonction sumOfOdds qui retourne la somme de tous les nombres impairs de 0 à n.
