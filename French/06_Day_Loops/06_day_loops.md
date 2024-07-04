<div align="center">
  <h1> 30 Days Of JavaScript: Loops</h1>
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

[<< Day 5](../05_Day_Arrays/05_day_arrays.md) | [Day 7 >>](../07_Day_Functions/07_day_functions.md)

![Day 5](../images/banners/day_1_6.png)

- [📔 Day 6](#-day-6)
  - [Loops](#loops)
    - [for Loop](#for-loop)
    - [while loop](#while-loop)
    - [do while loop](#do-while-loop)
    - [for of loop](#for-of-loop)
    - [break](#break)
    - [continue](#continue)
  - [💻 Exercises: Day 6](#-exercises-day-6)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# 📔 Day 6

## Loops

Les boucles sont utilisées pour exécuter un bloc de code à plusieurs reprises. JavaScript dispose de différentes sortes de boucles : `for`, `while`, `do while`, et `for of`.

### for Loop

La boucle `for` est la plus couramment utilisée en JavaScript. Elle a une syntaxe claire et simple.

```js
for(let i = 0; i <= 5; i++){
  console.log(i)
}

// 0 1 2 3 4 5
```

### while loop

La boucle `while` continue à exécuter un bloc de code tant que la condition spécifiée est vraie.

```js
let i = 0
while (i <= 5) {
  console.log(i)
  i++
}

// 0 1 2 3 4 5
```

### do while loop

La boucle `do while` est similaire à la boucle `while`, sauf qu'elle exécute le bloc de code au moins une fois avant de vérifier la condition.

```js
let i = 0
do {
  console.log(i)
  i++
} while (i <= 5)

// 0 1 2 3 4 5
```

### for of loop

La boucle `for of` est utilisée pour itérer sur des objets itérables (comme des tableaux ou des chaînes de caractères).

```js
let numbers = [1, 2, 3, 4, 5]
for (const num of numbers) {
  console.log(num)
}

// 1 2 3 4 5
```

### break

L'instruction `break` est utilisée pour arrêter une boucle avant qu'elle n'ait parcouru tous les éléments.

```js
for (let i = 0; i <= 5; i++) {
  if (i === 3) {
    break
  }
  console.log(i)
}

// 0 1 2
```

### continue

L'instruction `continue` est utilisée pour passer à l'itération suivante de la boucle.

```js
for (let i = 0; i <= 5; i++) {
  if (i === 3) {
    continue
  }
  console.log(i)
}

// 0 1 2 4 5
```

## 💻 Exercises: Day 6

### Exercises: Level 1

1. Itérez de 0 à 10 en utilisant une boucle `for`, `while`, et `do while`.
2. Itérez de 10 à 0 en utilisant une boucle `for`, `while`, et `do while`.

### Exercises: Level 2

1. Itérez de 0 à n en utilisant une boucle `for`.

### Exercises: Level 3

1. Créez une boucle qui génère le tableau suivant : `[[1, 1, 1], [2, 2, 2], [3, 3, 3], [4, 4, 4], [5, 5, 5], [6, 6, 6], [7, 7, 7], [8, 8, 8], [9, 9, 9], [10, 10, 10]]`.
2. Créez une boucle qui génère le tableau suivant : `[[0, 1, 2, 3, 4, 5], [0, 1, 2, 3, 4, 5], [0, 1, 2, 3, 4, 5], [0, 1, 2, 3, 4, 5], [0, 1, 2, 3, 4, 5]]`.
