<div align="center">
  <h1> 30 Days Of JavaScript: Conditionals</h1>
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

[<< Day 3](../03_Day_Booleans_operators_date/03_booleans_operators_date.md) | [Day 5 >>](../05_Day_Arrays/05_day_arrays.md)

![Thirty Days Of JavaScript](../images/banners/day_1_4.png)

- [📔 Day 4](#-day-4)
  - [Conditionals](#conditionals)
    - [If](#if)
    - [If Else](#if-else)
    - [If Else if Else](#if-else-if-else)
    - [Switch](#switch)
    - [Ternary Operators](#ternary-operators)
  - [💻 Exercises](#-exercises)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# 📔 Day 4

## Conditionals

Les conditionnels sont utilisés pour prendre des décisions en fonction de différentes conditions. Les instructions conditionnelles exécutent un bloc de code si une condition spécifiée est vraie.

### If

L'instruction `if` exécute un bloc de code si une condition spécifiée est vraie.

```js
let isRaining = true
if (isRaining) {
  console.log('N\'oubliez pas votre parapluie.')
}
```

### If Else

L'instruction `if...else` exécute un bloc de code si une condition est vraie, et un autre bloc de code si cette condition est fausse.

```js
let isRaining = false
if (isRaining) {
  console.log('N\'oubliez pas votre parapluie.')
} else {
  console.log('Pas besoin de parapluie.')
}
```

### If Else if Else

L'instruction `if...else if...else` exécute différents blocs de code en fonction de plusieurs conditions.

```js
let weather = 'ensoleillé'
if (weather === 'pluvieux') {
  console.log('N\'oubliez pas votre parapluie.')
} else if (weather === 'nuageux') {
  console.log('Il pourrait pleuvoir, prenez un parapluie.')
} else {
  console.log('Pas besoin de parapluie.')
}
```

### Switch

L'instruction `switch` est utilisée pour effectuer des actions différentes en fonction de différentes conditions.

```js
let day = 'lundi'
switch (day) {
  case 'lundi':
    console.log('Aujourd\'hui c\'est lundi.')
    break
  case 'mardi':
    console.log('Aujourd\'hui c\'est mardi.')
    break
  case 'mercredi':
    console.log('Aujourd\'hui c\'est mercredi.')
    break
  default:
    console.log('Ce jour n\'est pas reconnu.')
}
```

### Ternary Operators

L'opérateur ternaire est un raccourci pour l'instruction `if...else`.

```js
let isRaining = true
isRaining ? console.log('N\'oubliez pas votre parapluie.') : console.log('Pas besoin de parapluie.')
```

## 💻 Exercises

### Exercises: Level 1

1. Déclarez une variable nommée `age` et écrivez une condition qui vérifie si l'âge est supérieur ou égal à 18. Si l'âge est supérieur ou égal à 18, imprimez 'Vous êtes assez vieux pour conduire.' sinon imprimez 'Vous êtes trop jeune pour conduire.'

### Exercises: Level 2

1. Écrivez un programme qui vérifie la météo. Si c'est 'ensoleillé', imprimez 'Portez des lunettes de soleil.'. Si c'est 'pluvieux', imprimez 'Prenez un parapluie.'. Si c'est 'nuageux', imprimez 'Il pourrait pleuvoir, prenez un parapluie.'.

### Exercises: Level 3

1. Créez une fonction qui prend un nombre comme paramètre et vérifie si le nombre est pair ou impair.
```
