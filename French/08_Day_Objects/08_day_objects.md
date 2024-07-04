<div align="center">
  <h1> 30 Days Of JavaScript: Objects</h1>
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

[<< Day 7](../07_Day_Functions/07_day_functions.md) | [Day 9 >>](../09_Day_Higher_order_functions/09_day_higher_order_functions.md)

![Thirty Days Of JavaScript](../images/banners/day_1_8.png)

- [📔 Day 8](#-day-8)
  - [Scope](#scope)
    - [Window Global Object](#window-global-object)
    - [Global scope](#global-scope)
    - [Local scope](#local-scope)
- [📔 Object](#-object)
    - [Creating an empty object](#creating-an-empty-object)
    - [Creating an objecting with values](#creating-an-objecting-with-values)
    - [Getting values from an object](#getting-values-from-an-object)
    - [Creating object methods](#creating-object-methods)
    - [Setting new key for an object](#setting-new-key-for-an-object)
    - [Object Methods](#object-methods)
      - [Getting object keys using Object.keys()](#getting-object-keys-using-objectkeys)
      - [Getting object values using Object.values()](#getting-object-values-using-objectvalues)
      - [Getting object entries using Object.entries()](#getting-object-entries-using-objectentries)
      - [Checking properties using hasOwnProperty()](#checking-properties-using-hasownproperty)
  - [💻 Exercises](#-exercises)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# 📔 Day 8

## Scope

Le scope se réfère à la portée d'une variable, c'est-à-dire de quelle partie de votre programme vous pouvez accéder à une variable particulière. En JavaScript, le scope est soit global soit local.

### Window Global Object

L'objet global window est l'objet global par défaut dans le navigateur. Il représente la fenêtre du navigateur et chaque variable, fonction et objet global est une propriété de l'objet window. Cela signifie que les variables globales peuvent être accédées et modifiées à partir de n'importe quelle partie de votre code.

### Global scope

Les variables déclarées à l'extérieur de la fonction sont des variables globales et sont accessibles de n'importe où dans un fichier.

```js
let a = 'JavaScript'
let b = 10

function letsLearnScope() {
  console.log(a, b) // JavaScript 10
}
letsLearnScope()
console.log(a, b) // JavaScript 10
```

### Local scope

Les variables déclarées à l'intérieur d'une fonction en utilisant `var`, `let` ou `const` ne sont accessibles qu'à l'intérieur de cette fonction.

```js
function letsLearnScope() {
  let gravity = 9.81
  console.log(gravity) // 9.81
}

letsLearnScope()
console.log(gravity) // une erreur car la variable n'est pas accessible
```

# 📔 Object

Un objet est une collection de propriétés, et une propriété est une association entre un nom (ou clé) et une valeur. Une valeur de propriété peut être une fonction, ce qui est alors considéré comme une méthode de l'objet.

### Creating an empty object

L'objet peut être créé en utilisant les accolades `{}`.

```js
let person = {}
console.log(person) // {}
```

### Creating an objecting with values

Un objet peut être créé avec des valeurs.

```js
let person = {
  firstName: 'Asabeneh',
  lastName: 'Yetayeh',
  age: 250,
  country: 'Finland',
  city: 'Helsinki',
  skills: ['HTML', 'CSS', 'JS', 'React', 'Node', 'MongoDB', 'Python', 'D3.js'],
  isMarried: true
}
console.log(person)
```

### Getting values from an object

Les valeurs d'un objet peuvent être accédées en utilisant le point `.` ou les crochets `[]`.

```js
let person = {
  firstName: 'Asabeneh',
  lastName: 'Yetayeh',
  age: 250,
  country: 'Finland',
  city: 'Helsinki',
  skills: ['HTML', 'CSS', 'JS', 'React', 'Node', 'MongoDB', 'Python', 'D3.js'],
  isMarried: true
}
console.log(person.firstName) // Asabeneh
console.log(person['lastName']) // Yetayeh
```

### Creating object methods

Les méthodes sont des fonctions qui appartiennent à un objet.

```js
let person = {
  firstName: 'Asabeneh',
  lastName: 'Yetayeh',
  age: 250,
  country: 'Finland',
  city: 'Helsinki',
  skills: ['HTML', 'CSS', 'JS', 'React', 'Node', 'MongoDB', 'Python', 'D3.js'],
  isMarried: true,
  getFullName: function() {
    return `${this.firstName} ${this.lastName}`
  }
}

console.log(person.getFullName()) // Asabeneh Yetayeh
```

### Setting new key for an object

Les nouvelles clés peuvent être définies pour un objet en utilisant le point `.` ou les crochets `[]`.

```js
person.nationality = 'Ethiopian'
person['title'] = 'teacher'
person.skills.push('Meteor')
person.skills.push('SasS')

console.log(person)
```

### Object Methods

Il existe différents objets prédéfinis en JavaScript. Par exemple, `Object.keys()`, `Object.values()`, `Object.entries()`, `hasOwnProperty()` sont des méthodes prédéfinies.

#### Getting object keys using Object.keys()

La méthode `Object.keys()` renvoie un tableau contenant les clés de l'objet.

```js
const keys = Object.keys(person)
console.log(keys) // ['firstName', 'lastName', 'age', 'country', 'city', 'skills', 'isMarried', 'nationality', 'title']
```

#### Getting object values using Object.values()

La méthode `Object.values()` renvoie un tableau contenant les valeurs de l'objet.

```js
const values = Object.values(person)
console.log(values)
```

#### Getting object entries using Object.entries()

La méthode `Object.entries()` renvoie un tableau contenant des tableaux de paires clé-valeur.

```js
const entries = Object.entries(person)
console.log(entries)
```

#### Checking properties using hasOwnProperty()

La méthode `hasOwnProperty()` vérifie si l'objet a la propriété spécifiée.

```js
console.log(person.hasOwnProperty('firstName')) // true
console.log(person.hasOwnProperty('score')) // false
```

## 💻 Exercises

### Exercises: Level 1

1. Créez un objet `dog` avec des propriétés : nom, pattes, couleur, âge, et aboiement. La méthode aboiement doit renvoyer un woof woof.

```js
const dog = {
  name: 'Bobby',
  legs: 4,
  color: 'brown',
  age: 5,
  bark: function() {
    return 'woof woof'
  }
}

console.log(dog.bark()) // woof woof
```

### Exercises: Level 2

1. Créez un objet `personAccount`. Il a des propriétés `firstName`, `lastName`, `incomes`, `expenses` et des méthodes `totalIncome`, `totalExpense`, `accountInfo`, `addIncome`, `addExpense` et `accountBalance`.

```js
const personAccount = {
  firstName: 'John',
  lastName: 'Doe',
  incomes: [],
  expenses: [],
  totalIncome: function() {
    return this.incomes.reduce((acc, income) => acc + income, 0)
  },
  totalExpense: function() {
    return this.expenses.reduce((acc, expense) => acc + expense, 0)
  },
  accountInfo: function() {
    return `${this.firstName} ${this.lastName} a un revenu total de ${this.totalIncome()} et des dépenses totales de ${this.totalExpense()}.`
  },
  addIncome: function(amount) {
    this.incomes.push(amount)
  },
  addExpense: function(amount) {
    this.expenses.push(amount)
  },
  accountBalance: function() {
    return this.totalIncome() - this.totalExpense()
  }
}

personAccount.addIncome(2000)
personAccount.addIncome(

1500)
personAccount.addExpense(500)
personAccount.addExpense(200)

console.log(personAccount.accountInfo()) // John Doe a un revenu total de 3500 et des dépenses totales de 700.
console.log(personAccount.accountBalance()) // 2800
```

### Exercises: Level 3

1. Créez une méthode qui copie un objet sans modifier l'original.
2. Créez une méthode qui prend un objet et retourne un tableau de toutes les valeurs des propriétés de l'objet.

```js
function copyObject(obj) {
  return JSON.parse(JSON.stringify(obj))
}

const original = {a: 1, b: 2, c: 3}
const copy = copyObject(original)
console.log(copy) // {a: 1, b: 2, c: 3}

function getObjectValues(obj) {
  return Object.values(obj)
}

console.log(getObjectValues(original)) // [1, 2, 3]
```