<div align="center">
  <h1> 30 Days Of JavaScript: Sets and Maps</h1>
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

[<< Day 9](../09_Day_Higher_order_functions/09_day_higher_order_functions.md) | [Day 11>>](../11_Day_Destructuring_and_spreading/11_day_destructuring_and_spreading.md)

![Day 10](../images/banners/day_1_10.png)

- [Day 10](#day-10)
  - [Set](#set)
    - [Creating an empty set](#creating-an-empty-set)
    - [Creating set from array](#creating-set-from-array)
    - [Adding an element to a set](#adding-an-element-to-a-set)
    - [Deleting an element a set](#deleting-an-element-a-set)
    - [Checking an element in the set](#checking-an-element-in-the-set)
    - [Clearing the set](#clearing-the-set)
    - [Union of sets](#union-of-sets)
    - [Intersection of sets](#intersection-of-sets)
    - [Difference of sets](#difference-of-sets)
    - [Subset](#subset)
  - [Map](#map)
    - [Creating an empty map](#creating-an-empty-map)
    - [Creating a map from array](#creating-a-map-from-array)
    - [Adding values to the map](#adding-values-to-the-map)
    - [Getting a value from map](#getting-a-value-from-map)
    - [Checking key in map](#checking-key-in-map)
    - [Getting all values from map](#getting-all-values-from-map)
  - [💻 Exercises](#-exercises)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# Day 10

## Set

Un `Set` est une collection d'éléments uniques. Cela signifie qu'un set ne peut pas avoir de doublons.

### Creating an empty set

```js
const companies = new Set()
console.log(companies)
```

### Creating set from array

Nous pouvons créer un set à partir d'un tableau.

```js
const languages = [
  'English',
  'Finnish',
  'English',
  'French',
  'Spanish',
  'English',
  'French',
]
const setOfLanguages = new Set(languages)
console.log(setOfLanguages)
```

### Adding an element to a set

```js
const companies = new Set()
console.log(companies.size)

companies.add('Google')
companies.add('Facebook')
companies.add('Amazon')
companies.add('Oracle')
companies.add('Microsoft')

console.log(companies.size)
console.log(companies)
```

### Deleting an element a set

```js
console.log(companies.delete('Google'))
console.log(companies.size)
```

### Checking an element in the set

```js
console.log(companies.has('Apple'))
console.log(companies.has('Facebook'))
```

### Clearing the set

```js
companies.clear()
console.log(companies)
```

### Union of sets

Pour trouver l'union de deux sets, nous pouvons utiliser l'opérateur de spread.

```js
let a = [1, 2, 3, 4, 5]
let b = [3, 4, 5, 6]
let c = [...a, ...b]

let A = new Set(a)
let B = new Set(b)
let C = new Set(c)

console.log(C)
```

### Intersection of sets

Pour trouver l'intersection de deux sets, nous pouvons utiliser la méthode `filter`.

```js
let a = [1, 2, 3, 4, 5]
let b = [3, 4, 5, 6]

let A = new Set(a)
let B = new Set(b)

let c = a.filter((num) => B.has(num))
let C = new Set(c)

console.log(C)
```

### Difference of sets

Pour trouver la différence entre deux sets, nous pouvons utiliser la méthode `filter`.

```js
let a = [1, 2, 3, 4, 5]
let b = [3, 4, 5, 6]

let A = new Set(a)
let B = new Set(b)

let c = a.filter((num) => !B.has(num))
let C = new Set(c)

console.log(C)
```

### Subset

Pour vérifier si un set est un sous-ensemble d'un autre set, nous utilisons la méthode `every`.

```js
let a = [1, 2, 3, 4, 5]
let b = [3, 4, 5]

let A = new Set(a)
let B = new Set(b)

let isSubset = b.every((num) => A.has(num))
console.log(isSubset)
```

## Map

Un `Map` est une collection d'éléments avec une clé unique associée à chaque élément.

### Creating an empty map

```js
const map = new Map()
console.log(map)
```

### Creating a map from array

Nous pouvons créer un map à partir d'un tableau.

```js
const countries = [
  ['Finland', 'Helsinki'],
  ['Sweden', 'Stockholm'],
  ['Norway', 'Oslo'],
]
const map = new Map(countries)
console.log(map)
console.log(map.size)
```

### Adding values to the map

```js
const countriesMap = new Map()
console.log(countriesMap.size)

countriesMap.set('Finland', 'Helsinki')
countriesMap.set('Sweden', 'Stockholm')
countriesMap.set('Norway', 'Oslo')

console.log(countriesMap)
console.log(countriesMap.size)
```

### Getting a value from map

```js
console.log(countriesMap.get('Finland'))
```

### Checking key in map

```js
console.log(countriesMap.has('Finland'))
```

### Getting all values from map

```js
for (const country of countriesMap) {
  console.log(country)
}
```

## 💻 Exercises

### Exercises: Level 1

1. Créez un set vide.
2. Créez un set contenant 0 à 10 en utilisant la boucle `for`.

### Exercises: Level 2

1. Supprimez un élément d'un set.
2. Effacez un set.

### Exercises: Level 3

1. Créez un map des pays et des capitales.
2. Affichez tous les éléments du map.