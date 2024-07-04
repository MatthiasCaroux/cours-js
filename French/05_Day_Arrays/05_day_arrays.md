<div align="center">
  <h1> 30 Days Of JavaScript: Arrays</h1>
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

[<< Day 4](../04_Day_Conditionals/04_day_conditionals.md) | [Day 6 >>](../06_Day_Loops/06_day_loops.md)

![Day 5](../images/banners/day_1_5.png)

- [📔 Day 5](#-day-5)
  - [Arrays](#arrays)
    - [How to create an empty array](#how-to-create-an-empty-array)
    - [How to create an array with values](#how-to-create-an-array-with-values)
    - [Creating an array using split](#creating-an-array-using-split)
    - [Accessing array items using index](#accessing-array-items-using-index)
    - [Modifying array element](#modifying-array-element)
    - [Methods to manipulate an array](#methods-to-manipulate-an-array)
      - [Array constructor](#array-constructor)
      - [Creating static values with fill](#creating-static-values-with-fill)
      - [Concatenating array using concat](#concatenating-array-using-concat)
      - [Getting array length](#getting-array-length)
      - [Getting index an element in arr array](#getting-index-an-element-in-arr-array)
      - [Check an element if it exist in an array](#check-an-element-if-it-exist-in-an-array)
      - [Getting last index of an element in array](#getting-last-index-of-an-element-in-array)
      - [Includes](#includes)
      - [Checking array](#checking-array)
      - [Converting array to string](#converting-array-to-string)
      - [Joining array elements](#joining-array-elements)
      - [Slice array elements](#slice-array-elements)
      - [Splice method in array](#splice-method-in-array)
      - [Adding item to an array using push](#adding-item-to-an-array-using-push)
      - [Removing the end element using pop](#removing-the-end-element-using-pop)
      - [Removing an element from the beginning](#removing-an-element-from-the-beginning)
      - [Add an element from the beginning](#add-an-element-from-the-beginning)
      - [Reversing array order](#reversing-array-order)
      - [Sorting elements in array](#sorting-elements-in-array)
    - [Array of arrays](#array-of-arrays)
  - [💻 Exercises](#-exercises)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# 📔 Day 5

## Arrays

Un tableau est une structure de données spéciale qui permet de stocker plusieurs valeurs dans une seule variable. Il est utilisé pour stocker des collections d'éléments.

### How to create an empty array

Nous pouvons créer un tableau vide de différentes manières.

```js
// en utilisant le constructeur Array
let arr = Array()

// ou en utilisant des crochets
let arr = []
```

### How to create an array with values

Nous pouvons stocker des valeurs de différentes données dans un tableau. Voici un exemple :

```js
let numbers = [0, 3.14, 9.81, 37, 98.6, 100] // tableau de nombres
let fruits = ['banana', 'orange', 'mango', 'lemon'] // tableau de strings, fruits
let vegetables = ['Tomato', 'Potato', 'Cabbage', 'Onion', 'Carrot']
let animalProducts = ['milk', 'meat', 'butter', 'yoghurt']
let webTechs = ['HTML', 'CSS', 'JS', 'React', 'Redux', 'Node', 'MongDB']
let countries = ['Finland', 'Denmark', 'Sweden', 'Norway', 'Iceland']

// imprimez le tableau et son longueur
console.log('Numbers:', numbers)
console.log('Number of numbers:', numbers.length)

console.log('Fruits:', fruits)
console.log('Number of fruits:', fruits.length)

console.log('Vegetables:', vegetables)
console.log('Number of vegetables:', vegetables.length)

console.log('Animal products:', animalProducts)
console.log('Number of animal products:', animalProducts.length)

console.log('Web technologies:', webTechs)
console.log('Number of web technologies:', webTechs.length)

console.log('Countries:', countries)
console.log('Number of countries:', countries.length)
```

### Creating an array using split

Comme les chaînes de caractères sont des itérables, nous pouvons convertir une chaîne en tableau en utilisant la méthode split.

```js
let js = 'JavaScript'
const charsInJavaScript = js.split('')

console.log(charsInJavaScript)

let companiesString = 'Facebook, Google, Microsoft, Apple, IBM, Oracle, Amazon'
const companies = companiesString.split(',')

console.log(companies)
```

### Accessing array items using index

Nous pouvons accéder à chaque élément du tableau en utilisant l'index. Les index dans un tableau commencent à partir de zéro.

```js
let fruits = ['banana', 'orange', 'mango', 'lemon']
let firstFruit = fruits[0] // accéder au premier élément en utilisant son index

console.log(firstFruit) // banana

secondFruit = fruits[1]
console.log(secondFruit) // orange

lastFruit = fruits[3]
console.log(lastFruit) // lemon

// Dernier index peut être calculé comme suit
let lastIndex = fruits.length - 1
lastFruit = fruits[lastIndex]

console.log(lastFruit)  // lemon
```

### Modifying array element

Un tableau est mutable (modifiable). Une fois un tableau créé, nous pouvons modifier les éléments du tableau.

```js
let numbers = [1, 2, 3, 4, 5]
numbers[0] = 10      // changement 1 à 10
numbers[1] = 20      // changement  2 à 20

console.log(numbers) // [10, 20, 3, 4, 5]
```

### Methods to manipulate an array

Il existe différentes méthodes pour manipuler un tableau. Les méthodes peuvent être classées en fonction de leur fonction : ajouter des éléments, supprimer des éléments, etc.

#### Array constructor

La méthode Array permet de créer un tableau.

```js
const arr = Array() // crée un tableau vide
console.log(arr)

let eightEmptyValues = Array(8) // il crée huit emplacements vides
console.log(eightEmptyValues) // [empty x 8]
```

#### Creating static values with fill

La méthode fill permet de remplir un tableau avec une valeur statique.

```js
const arr = Array(8).fill('X')
console.log(arr) // ['X', 'X', 'X', 'X', 'X', 'X', 'X', 'X']

const four4Values = Array(4).fill(4)
console.log(four4Values) // [4, 4, 4, 4]
```

#### Concatenating array using concat

La méthode concat permet de concaténer deux tableaux.

```js
const firstList = [1, 2, 3]
const secondList = [4, 5, 6]
const thirdList = firstList.concat(secondList)

console.log(thirdList) // [1, 2, 3, 4, 5, 6]
```

#### Getting array length

La longueur d'un tableau peut être obtenue en utilisant la propriété length.

```js
const numbers = [1, 2, 3, 4, 5]
console.log(numbers.length) // 5
```

#### Getting index an element in arr array

Pour obtenir l'index d'un élément dans un tableau, nous utilisons la méthode indexOf. Si l'élément existe dans le tableau, il retourne l'index sinon il retourne -1.

```js
const numbers = [1, 2, 3, 4, 5]

console.log(numbers.indexOf(5)) // 4
console.log(numbers.indexOf(0)) // -1
console.log(numbers.indexOf(1)) // 0
console.log(numbers.indexOf(6)) // -1
```

#### Check an element if it exist in an array

Pour vérifier si un élément existe dans un tableau, nous utilisons la méthode include qui retourne un booléen.

```js
const numbers = [1, 2, 3, 4, 5]

console.log(numbers.includes

(5)) // true
console.log(numbers.includes(0)) // false
console.log(numbers.includes(1)) // true
console.log(numbers.includes(6)) // false
```

#### Getting last index of an element in array

Pour trouver le dernier index d'un élément dans un tableau, nous utilisons la méthode lastIndexOf. Cette méthode retourne le dernier index si l'élément existe dans le tableau et retourne -1 si l'élément n'existe pas dans le tableau.

```js
const numbers = [1, 2, 3, 4, 5, 3, 1, 2, 3]

console.log(numbers.lastIndexOf(2)) // 7
console.log(numbers.lastIndexOf(0)) // -1
console.log(numbers.lastIndexOf(1)) // 6
console.log(numbers.lastIndexOf(4)) // 3
console.log(numbers.lastIndexOf(6)) // -1
```

#### Includes

Pour vérifier si un élément existe dans un tableau, nous utilisons la méthode includes. Si l'élément existe dans le tableau, il retourne true sinon il retourne false.

```js
const numbers = [1, 2, 3, 4, 5]

console.log(numbers.includes(5)) // true
console.log(numbers.includes(0)) // false
console.log(numbers.includes(1)) // true
console.log(numbers.includes(6)) // false
```

#### Checking array

Pour vérifier si la variable est un tableau, nous utilisons Array.isArray.

```js
const numbers = [1, 2, 3, 4, 5]
console.log(Array.isArray(numbers)) // true

const number = 100
console.log(Array.isArray(number)) // false
```

#### Converting array to string

Pour convertir un tableau en chaîne de caractères, nous utilisons la méthode toString.

```js
const numbers = [1, 2, 3, 4, 5]
console.log(numbers.toString()) // 1,2,3,4,5

const names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']
console.log(names.toString()) // Asabeneh,Mathias,Elias,Brook
```

#### Joining array elements

Pour joindre les éléments d'un tableau, nous utilisons la méthode join. Par défaut, il utilise une virgule comme séparateur mais nous pouvons passer un séparateur différent.

```js
const numbers = [1, 2, 3, 4, 5]
console.log(numbers.join()) // 1,2,3,4,5

const names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']
console.log(names.join()) // Asabeneh,Mathias,Elias,Brook
console.log(names.join('')) // AsabenehMathiasEliasBrook
console.log(names.join(' ')) // Asabeneh Mathias Elias Brook
console.log(names.join(', ')) // Asabeneh, Mathias, Elias, Brook
console.log(names.join(' # ')) // Asabeneh # Mathias # Elias # Brook
```

#### Slice array elements

Pour couper plusieurs éléments d'un tableau, nous utilisons la méthode slice. Elle prend deux arguments : le début et la fin de l'index.

```js
const numbers = [1, 2, 3, 4, 5]
console.log(numbers.slice()) // [1, 2, 3, 4, 5]
console.log(numbers.slice(0, numbers.length)) // [1, 2, 3, 4, 5]
console.log(numbers.slice(1, 4)) // [2, 3, 4]
```

#### Splice method in array

Pour ajouter ou retirer des éléments d'un tableau, nous utilisons la méthode splice. Elle prend trois arguments : la position de départ, le nombre d'éléments à retirer, et les éléments à ajouter.

```js
const numbers = [1, 2, 3, 4, 5]
console.log(numbers.splice()) // []
```

#### Adding item to an array using push

Pour ajouter un élément à la fin d'un tableau, nous utilisons la méthode push.

```js
const arr = ['item1', 'item2', 'item3']
arr.push('new item')
console.log(arr) // ['item1', 'item2', 'item3', 'new item']
```

#### Removing the end element using pop

Pour retirer un élément à la fin d'un tableau, nous utilisons la méthode pop.

```js
const numbers = [1, 2, 3, 4, 5]
numbers.pop() // 5 est retiré du dernier index
console.log(numbers) // [1, 2, 3, 4]
```

#### Removing an element from the beginning

Pour retirer un élément du début d'un tableau, nous utilisons la méthode shift.

```js
const numbers = [1, 2, 3, 4, 5]
numbers.shift() // 1 est retiré du premier index
console.log(numbers) // [2, 3, 4, 5]
```

#### Add an element from the beginning

Pour ajouter un élément au début d'un tableau, nous utilisons la méthode unshift.

```js
const numbers = [1, 2, 3, 4, 5]
numbers.unshift(0) // ajoute zéro au début
console.log(numbers) // [0, 1, 2, 3, 4, 5]
```

#### Reversing array order

Pour inverser l'ordre des éléments d'un tableau, nous utilisons la méthode reverse.

```js
const numbers = [1, 2, 3, 4, 5]
numbers.reverse() // [5, 4, 3, 2, 1]
console.log(numbers)
```

#### Sorting elements in array

Pour trier les éléments d'un tableau, nous utilisons la méthode sort. Par défaut, elle trie les valeurs comme des chaînes de caractères.

```js
const webTechs = ['HTML', 'CSS', 'JavaScript', 'React', 'Redux', 'Node', 'MongoDB']
webTechs.sort()
console.log(webTechs) // ['CSS', 'HTML', 'JavaScript', 'MongoDB', 'Node', 'React', 'Redux']
```

### Array of arrays

Un tableau peut contenir d'autres tableaux. Nous appelons un tableau qui contient d'autres tableaux un tableau multidimensionnel.

```js
const firstNums = [1, 2, 3]
const secondNums = [1, 4, 9]

const arrayOfArray =  [[1, 2, 3], [1, 2, 3]]
console.log(arrayOfArray[0]) // [1, 2, 3]
```

## 💻 Exercises

### Exercises: Level 1

1. Déclarez un tableau vide.
2. Déclarez un tableau avec plus de 5 éléments et trouvez la longueur de ce tableau.

### Exercises: Level 2

1. Trouvez le premier élément, le milieu et le dernier élément du tableau que vous avez déclaré à l'exercice 2.

### Exercises: Level 3

1. Créez un tableau de tableaux, où chaque tableau contient un prénom, un nom et une adresse email.
2. Triez ce tableau de tableaux par ordre alphabétique des prénoms.
