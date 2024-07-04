<div align="center">
  <h1> 30 Days Of JavaScript: Booleans, Operators, Date</h1>
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

[<< Day 2](../02_Day_Data_types/02_day_data_types.md) | [Day 4 >>](../04_Day_Conditionals/04_day_conditionals.md)

![Thirty Days Of JavaScript](../images/banners/day_1_3.png)

- [📔 Day 3](#-day-3)
  - [Booleans](#booleans)
  - [Truthy values](#truthy-values)
  - [Falsy values](#falsy-values)
  - [Undefined](#undefined)
  - [Null](#null)
  - [Operators](#operators)
    - [Assignment operators](#assignment-operators)
    - [Arithmetic operators](#arithmetic-operators)
    - [Comparison operators](#comparison-operators)
    - [Logical operators](#logical-operators)
    - [Increment operator](#increment-operator)
    - [Decrement operator](#decrement-operator)
    - [Ternary operators](#ternary-operators)
  - [Operator Precedence](#operator-precedence)
  - [Date Object](#date-object)
  - [Exercises](#exercises)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# 📔 Day 3

## Booleans

Un booléen est un type de données qui représente l'une des deux valeurs : vrai (true) ou faux (false). Les valeurs booléennes sont utiles dans la prise de décision ou dans les vérifications.

```js
let isLightOn = true
let isRaining = false
let isHungry = true
let isMarried = false
```

## Truthy values

Dans JavaScript, une valeur est dite truthy si elle est évaluée comme vraie dans un contexte booléen. Les valeurs suivantes sont évaluées comme vraies :

- Tous les nombres positifs et négatifs (sauf zéro)
- Toutes les chaînes de caractères non vides
- L'objet 'true'

```js
// Exemples de valeurs truthy
console.log(Boolean(1))  // true
console.log(Boolean('non-vide')) // true
console.log(Boolean(true)) // true
```

## Falsy values

Une valeur est dite falsy si elle est évaluée comme fausse. Les valeurs suivantes sont falsy :

- 0
- ''
- null
- undefined
- NaN
- false

```js
// Exemples de valeurs falsy
console.log(Boolean(0))  // false
console.log(Boolean('')) // false
console.log(Boolean(null)) // false
console.log(Boolean(undefined)) // false
console.log(Boolean(NaN)) // false
console.log(Boolean(false)) // false
```

## Undefined

Le mot clé `undefined` est un littéral utilisé lorsqu'une variable n'a pas été assignée à une valeur.

```js
let firstName
console.log(firstName) // undefined, parce que ce n'est pas assigné à une valeur encore
```

## Null

`null` en JavaScript signifie une valeur vide ou inconnue.

```js
let empty = null
console.log(empty) // null
```

## Operators

Les opérateurs sont des symboles qui sont utilisés pour effectuer des opérations sur des valeurs ou des variables. Voici une liste de types d'opérateurs en JavaScript :

### Assignment operators

Les opérateurs d'affectation sont utilisés pour assigner des valeurs aux variables.

```js
let x = 10
let y = 5
```

### Arithmetic operators

Les opérateurs arithmétiques sont utilisés pour effectuer des calculs mathématiques.

```js
let sum = x + y
let diff = x - y
let mult = x * y
let div = x / y
let remainder = x % y
```

### Comparison operators

Les opérateurs de comparaison sont utilisés pour comparer deux valeurs. Ils retournent un booléen soit vrai soit faux.

```js
console.log(x == y)  // false
console.log(x === y) // false
console.log(x != y)  // true
console.log(x > y)   // true
console.log(x >= y)  // true
console.log(x < y)   // false
console.log(x <= y)  // false
```

### Logical operators

Les opérateurs logiques sont utilisés pour combiner deux ou plusieurs conditions booléennes.

```js
console.log(x > y && y > 0)  // true
console.log(x > y || y < 0)  // true
console.log(!(x > y))        // false
```

### Increment operator

L'opérateur d'incrémentation augmente la valeur d'une variable d'une unité.

```js
let count = 0
count++
console.log(count) // 1
```

### Decrement operator

L'opérateur de décrémentation diminue la valeur d'une variable d'une unité.

```js
let count = 0
count--
console.log(count) // -1
```

### Ternary operators

L'opérateur ternaire est utilisé pour effectuer une opération conditionnelle en une seule ligne.

```js
let isRaining = true
isRaining ? console.log('Vous avez besoin d\'un parapluie.') : console.log('Pas besoin de parapluie.')
```

## Operator Precedence

La priorité des opérateurs détermine l'ordre dans lequel les opérateurs sont évalués. Par exemple, les opérateurs arithmétiques ont une priorité plus élevée que les opérateurs de comparaison.

## Date Object

Le `Date` object en JavaScript est utilisé pour travailler avec les dates et les heures.

```js
const now = new Date()
console.log(now) // affiche la date et l'heure actuelles
```

## Exercises

### Exercises: Level 1

1. Déclarez une variable nommée `isSunny` et assignez-lui la valeur `true`.
2. Déclarez une variable nommée `isWindy` et assignez-lui la valeur `false`.

### Exercises: Level 2

1. Comparez deux valeurs en utilisant les opérateurs de comparaison et imprimez les résultats.

### Exercises: Level 3

1. Créez une fonction qui prend deux paramètres et renvoie leur somme.
2. Créez une fonction qui prend une date comme paramètre et renvoie le jour de la semaine correspondant.
```
