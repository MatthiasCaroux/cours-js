<div align="center">
  <h1> 30 Days Of JavaScript: Error handling</h1>
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

[<< Day 13](../13_Day_Console_object_methods/13_day_console_object_methods.md) | [Day 15>>](../15_Day_Classes/15_day_classes.md)

![Thirty Days Of JavaScript](../images/banners/day_1_14.png)

- [Day 14](#day-14)
  - [Error Handling](#error-handling)
    - [Error Types](#error-types)
  - [Exercises](#exercises)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# Day 14

## Error Handling

La gestion des erreurs est importante pour rendre votre code plus robuste et fiable. JavaScript fournit un moyen de gérer les erreurs à l'aide des blocs `try`, `catch` et `finally`.

```js
try {
  // code qui peut potentiellement lever une exception
} catch (err) {
  // code à exécuter en cas d'erreur
} finally {
  // code à exécuter après le bloc try ou catch, qu'il y ait eu une erreur ou non
}
```

### Error Types

JavaScript possède plusieurs types d'erreurs intégrés que vous pouvez rencontrer en programmant :

1. **SyntaxError** : Une erreur de syntaxe détectée lors de l'analyse du code.
2. **ReferenceError** : Une erreur lorsque vous référencez une variable qui n'existe pas.
3. **TypeError** : Une erreur lorsque vous essayez d'utiliser une valeur d'une manière qui n'est pas permise.
4. **RangeError** : Une erreur lorsque vous utilisez un nombre qui est en dehors de la plage des valeurs permises.
5. **EvalError** : Une erreur concernant la fonction `eval()`.

Voici des exemples de ces erreurs :

```js
// SyntaxError
try {
  eval('let a = 2')
} catch (err) {
  console.error(err) // SyntaxError: Unexpected identifier
}

// ReferenceError
try {
  console.log(b)
} catch (err) {
  console.error(err) // ReferenceError: b is not defined
}

// TypeError
try {
  let num = 10
  num.toUpperCase()
} catch (err) {
  console.error(err) // TypeError: num.toUpperCase is not a function
}

// RangeError
try {
  let num = 1
  num.toPrecision(500)
} catch (err) {
  console.error(err) // RangeError: toPrecision() argument must be between 1 and 100
}

// EvalError
try {
  eval('foo bar')
} catch (err) {
  console.error(err) // EvalError: Unexpected identifier
}
```

## Exercises

### Exercises: Level 1

1. Utilisez un bloc `try` et `catch` pour attraper une erreur syntaxique.
2. Utilisez un bloc `try` et `catch` pour attraper une erreur de référence.

### Exercises: Level 2

1. Créez une fonction qui déclenche une erreur de type `TypeError`.
2. Créez une fonction qui déclenche une erreur de type `RangeError`.

### Exercises: Level 3

1. Créez une fonction qui déclenche une erreur de type `SyntaxError` en utilisant la fonction `eval()`.
2. Créez une fonction qui déclenche une erreur de type `EvalError`.