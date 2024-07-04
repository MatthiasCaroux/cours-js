<div align="center">
  <h1> 30 Days Of JavaScript: Higher Order Functions</h1>
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

[<< Day 8](../08_Day_Objects/08_day_objects.md) | [Day 10 >>](../10_Day_Sets_and_Maps/10_day_Sets_and_Maps.md)

![Day 5](../images/banners/day_1_9.png)

- [Day 9](#day-9)
  - [Higher Order Function](#higher-order-function)
    - [Callback](#callback)
    - [Returning function](#returning-function)
    - [Setting time](#setting-time)
      - [Setting Interval using a setInterval function](#setting-interval-using-a-setinterval-function)
      - [Setting Timeout using a setTimeout function](#setting-timeout-using-a-settimeout-function)
  - [Functional Programming](#functional-programming)
    - [forEach](#foreach)
    - [map](#map)
    - [filter](#filter)
    - [reduce](#reduce)
    - [find](#find)
    - [findIndex](#findindex)
    - [some](#some)
    - [every](#every)
    - [sort](#sort)
  - [💻 Exercises](#-exercises)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# Day 9

## Higher Order Function

Une fonction de niveau supérieur est une fonction qui prend une autre fonction comme paramètre ou qui renvoie une fonction en sortie. JavaScript prend en charge les fonctions de niveau supérieur et les fonctions de rappel.

### Callback

Une fonction de rappel est une fonction passée en argument dans une autre fonction pour être exécutée plus tard.

```js
const callback = (n) => {
  return n ** 2
}

function cube(callback, n) {
  return callback(n) * n
}

console.log(cube(callback, 3))
```

### Returning function

Les fonctions de niveau supérieur peuvent également renvoyer une fonction.

```js
const higherOrder = n => {
  const doSomething = m => {
    const doWhatEver = t => {
      return 2 * n + 3 * m + t
    }
    return doWhatEver
  }
  return doSomething
}
console.log(higherOrder(2)(3)(10))
```

### Setting time

Les fonctions de rappel peuvent être utilisées pour exécuter des tâches après un certain temps. Les méthodes `setInterval` et `setTimeout` sont utilisées pour planifier des tâches en JavaScript.

#### Setting Interval using a setInterval function

```js
function sayHello() {
  console.log('Hello')
}
setInterval(sayHello, 1000) // cela s'exécute chaque seconde
```

#### Setting Timeout using a setTimeout function

```js
function sayGoodbye() {
  console.log('Goodbye')
}
setTimeout(sayGoodbye, 2000) // cela s'exécute après 2 secondes
```

## Functional Programming

La programmation fonctionnelle est un paradigme de programmation qui consiste à utiliser des fonctions pour traiter les données. Les fonctions d'ordre supérieur sont une partie importante de la programmation fonctionnelle. JavaScript prend en charge plusieurs méthodes de programmation fonctionnelle, telles que `forEach`, `map`, `filter`, `reduce`, `find`, `findIndex`, `some`, `every` et `sort`.

### forEach

La méthode `forEach` exécute une fonction donnée sur chaque élément du tableau.

```js
const numbers = [1, 2, 3, 4, 5]
numbers.forEach(num => console.log(num))
```

### map

La méthode `map` crée un nouveau tableau en appliquant une fonction à chaque élément du tableau d'origine.

```js
const numbers = [1, 2, 3, 4, 5]
const numbersSquare = numbers.map(num => num ** 2)
console.log(numbersSquare)
```

### filter

La méthode `filter` crée un nouveau tableau avec tous les éléments qui passent le test implémenté par la fonction fournie.

```js
const countries = ['Finland', 'Sweden', 'Denmark', 'Norway', 'Iceland']
const countriesContainingLand = countries.filter(country => country.includes('land'))
console.log(countriesContainingLand)
```

### reduce

La méthode `reduce` applique une fonction à un accumulateur et à chaque valeur du tableau (de gauche à droite) pour la réduire à une seule valeur.

```js
const numbers = [1, 2, 3, 4, 5]
const sum = numbers.reduce((acc, curr) => acc + curr, 0)
console.log(sum)
```

### find

La méthode `find` renvoie la première valeur du tableau qui satisfait la fonction de test fournie. Sinon, elle renvoie `undefined`.

```js
const numbers = [1, 2, 3, 4, 5]
const firstEvenNumber = numbers.find(num => num % 2 === 0)
console.log(firstEvenNumber)
```

### findIndex

La méthode `findIndex` renvoie l'index du premier élément du tableau qui satisfait la fonction de test fournie. Sinon, elle renvoie `-1`.

```js
const numbers = [1, 2, 3, 4, 5]
const firstEvenNumberIndex = numbers.findIndex(num => num % 2 === 0)
console.log(firstEvenNumberIndex)
```

### some

La méthode `some` teste si au moins un élément du tableau satisfait la fonction de test fournie. Elle renvoie un booléen.

```js
const numbers = [1, 2, 3, 4, 5]
const hasEvenNumber = numbers.some(num => num % 2 === 0)
console.log(hasEvenNumber)
```

### every

La méthode `every` teste si tous les éléments du tableau satisfont la fonction de test fournie. Elle renvoie un booléen.

```js
const numbers = [1, 2, 3, 4, 5]
const allEvenNumbers = numbers.every(num => num % 2 === 0)
console.log(allEvenNumbers)
```

### sort

La méthode `sort` trie les éléments du tableau et renvoie le tableau trié.

```js
const products = ['Milk', 'Coffee', 'Sugar', 'Honey', 'Apple', 'Carrot']
console.log(products.sort())
```

## 💻 Exercises

### Exercises: Level 1

1. Utilisez la méthode `forEach` pour itérer sur un tableau de nombres et imprimez chaque nombre.
2. Utilisez la méthode `map` pour créer un nouveau tableau en élevant chaque nombre au carré.

### Exercises: Level 2

1. Utilisez la méthode `filter` pour filtrer les pays contenant 'land'.
2. Utilisez la méthode `reduce` pour trouver la somme des nombres.

### Exercises: Level 3

1. Utilisez la méthode `find` pour trouver le premier pays qui contient seulement six lettres.
2. Utilisez la méthode `findIndex` pour trouver la position du premier pays qui contient seulement six lettres.
