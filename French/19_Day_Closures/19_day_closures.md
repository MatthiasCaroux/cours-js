<div align="center">
  <h1> 30 Days Of JavaScript: Closures</h1>
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

[<< Day 18](../18_Day_Promises/18_day_promises.md) | [Day 20 >>](../20_Day_Writing_clean_codes/20_day_writing_clean_codes.md)

![Thirty Days Of JavaScript](../images/banners/day_1_19.png)

- [Day 19](#day-19)
  - [Closure](#closure)
  - [💻 Exercises](#-exercises)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# Day 19

## Closure

Les fermetures (closures) sont une fonctionnalité puissante de JavaScript qui permet à une fonction de se souvenir et d'accéder à son scope lexical, même lorsqu'elle est exécutée en dehors de ce scope. Une fermeture est créée lorsqu'une fonction est définie à l'intérieur d'une autre fonction, permettant à la fonction interne d'accéder aux variables de la fonction externe.

```js
function outerFunction() {
  let count = 0;

  function innerFunction() {
    count++;
    return count;
  }

  return innerFunction;
}

const increment = outerFunction();

console.log(increment()); // 1
console.log(increment()); // 2
console.log(increment()); // 3
```

Dans cet exemple, `innerFunction` est une fermeture qui capture la variable `count` de `outerFunction`. Même après que `outerFunction` a terminé son exécution, `innerFunction` peut toujours accéder et modifier `count`.

## 💻 Exercises

### Exercises: Level 1

1. Écrivez une fonction qui crée une fermeture et renvoie une fonction qui incrémente une variable de compteur.

```js
function createCounter() {
  let count = 0;
  return function() {
    count++;
    return count;
  };
}

const counter = createCounter();
console.log(counter()); // 1
console.log(counter()); // 2
console.log(counter()); // 3
```

### Exercises: Level 2

1. Modifiez l'exercice précédent pour ajouter un paramètre de pas, permettant à la fonction de fermeture d'incrémenter le compteur de ce pas.

```js
function createCounter(step) {
  let count = 0;
  return function() {
    count += step;
    return count;
  };
}

const counter = createCounter(2);
console.log(counter()); // 2
console.log(counter()); // 4
console.log(counter()); // 6
```

### Exercises: Level 3

1. Écrivez une fonction qui crée une fermeture et renvoie un objet avec deux méthodes : `increment` et `decrement`, qui incrémentent et décrémentent une variable de compteur, respectivement.

```js
function createCounter() {
  let count = 0;
  return {
    increment: function() {
      count++;
      return count;
    },
    decrement: function() {
      count--;
      return count;
    }
  };
}

const counter = createCounter();
console.log(counter.increment()); // 1
console.log(counter.increment()); // 2
console.log(counter.decrement()); // 1