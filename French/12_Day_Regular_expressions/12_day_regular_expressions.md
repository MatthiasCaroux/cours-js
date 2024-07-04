<div align="center">
  <h1> 30 Days Of JavaScript: Regular Expressions</h1>
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

[<< Day 11](../11_Day_Destructuring_and_spreading/11_day_destructuring_and_spreading.md) | [Day 13>>](../13_Day_Console_object_methods/13_day_console_object_methods.md)

![Thirty Days Of JavaScript](../images/banners/day_1_12.png)

- [📘 Day 12](#-day-12)
  - [Regular Expressions](#regular-expressions)
    - [RegExp parameters](#regexp-parameters)
      - [Pattern](#pattern)
      - [Flags](#flags)
    - [Creating a pattern with RegExp Constructor](#creating-a-pattern-with-regexp-constructor)
    - [Creating a pattern without RegExp Constructor](#creating-a-pattern-without-regexp-constructor)
    - [RegExp object methods](#regexp-object-methods)
      - [Testing for a match](#testing-for-a-match)
      - [Array containing all matches](#array-containing-all-matches)
      - [Replacing a substring](#replacing-a-substring)
  - [💻 Exercises](#-exercises)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# 📘 Day 12

## Regular Expressions

Les expressions régulières sont des motifs utilisés pour correspondre à des combinaisons de caractères dans des chaînes de caractères. En JavaScript, les expressions régulières sont des objets qui peuvent être utilisés pour effectuer des recherches, des correspondances et des remplacements dans des chaînes de caractères.

### RegExp parameters

Les expressions régulières utilisent deux types de paramètres : `pattern` et `flags`.

#### Pattern

Un motif est une séquence de caractères qui forme un modèle de recherche.

#### Flags

Les drapeaux (flags) sont des marqueurs qui indiquent la manière dont une expression régulière doit être évaluée. Les drapeaux les plus couramment utilisés sont :

- `g`: global - recherche dans toute la chaîne
- `i`: case insensitive - insensible à la casse
- `m`: multiline - recherche sur plusieurs lignes

### Creating a pattern with RegExp Constructor

Les expressions régulières peuvent être créées en utilisant le constructeur RegExp.

```js
let pattern = 'love'
let regEx = new RegExp(pattern)
```

### Creating a pattern without RegExp Constructor

Les expressions régulières peuvent également être créées sans utiliser le constructeur RegExp.

```js
let regEx = /love/g
```

### RegExp object methods

Les expressions régulières en JavaScript disposent de plusieurs méthodes.

#### Testing for a match

La méthode `test()` teste une correspondance dans une chaîne de caractères. Elle retourne `true` ou `false`.

```js
const str = 'I love JavaScript'
const pattern = /love/
const result = pattern.test(str)

console.log(result) // true
```

#### Array containing all matches

La méthode `match()` recherche une correspondance dans une chaîne de caractères. Elle retourne un tableau contenant toutes les correspondances.

```js
const str = 'I love JavaScript. If you do not love JavaScript, what else can you love.'
const pattern = /love/g
const result = str.match(pattern)

console.log(result) // ["love", "love", "love"]
```

#### Replacing a substring

La méthode `replace()` remplace une correspondance par une autre chaîne de caractères.

```js
const txt = 'Python is the most beautiful language that a human begin has ever created. I recommend python for a first programming language'

const matchReplaced = txt.replace(/Python|python/, 'JavaScript')

console.log(matchReplaced)
// JavaScript is the most beautiful language that a human begin has ever created. I recommend python for a first programming language
```

## 💻 Exercises

### Exercises: Level 1

1. Écrivez une expression régulière pour correspondre au mot 'love' dans la chaîne 'I love JavaScript'.
2. Utilisez la méthode `test()` pour vérifier si 'Python' est dans la chaîne 'I love Python'.

### Exercises: Level 2

1. Écrivez une fonction qui prend une chaîne de caractères et renvoie le nombre de voyelles dans la chaîne.
2. Utilisez une expression régulière pour trouver toutes les occurrences du mot 'JavaScript' dans une chaîne de caractères.

### Exercises: Level 3

1. Écrivez une fonction qui valide une adresse email en utilisant une expression régulière.
2. Écrivez une fonction qui valide un numéro de téléphone en utilisant une expression régulière.