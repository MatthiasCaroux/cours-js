<div align="center">
  <h1> 30 Days Of JavaScript: Document Object Model(DOM)</h1>
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

[<< Day 20](../20_Day_Writing_clean_codes/20_day_writing_clean_codes.md) | [Day 22 >>](../22_Day_Manipulating_DOM_object/22_day_manipulating_DOM_object.md)

![Thirty Days Of JavaScript](../images/banners/day_1_21.png)

- [Day 21](#day-21)
  - [Document Object Model (DOM) - Day 1](#document-object-model-dom---day-1)
    - [Getting Element](#getting-element)
      - [Getting elements by tag name](#getting-elements-by-tag-name)
      - [Getting elements by class name](#getting-elements-by-class-name)
      - [Getting an element by id](#getting-an-element-by-id)
    - [Getting elements by using querySelector methods](#getting-elements-by-using-queryselector-methods)
      - [Getting an element by querySelector](#getting-an-element-by-queryselector)
      - [Getting elements by querySelectorAll](#getting-elements-by-queryselectorall)
    - [Adding attribute](#adding-attribute)
    - [Adding text to HTML element](#adding-text-to-html-element)
    - [Adding styles to HTML element](#adding-styles-to-html-element)
      - [Adding style color](#adding-style-color)
      - [Adding background color](#adding-background-color)
      - [Adding font-size](#adding-font-size)
      - [Adding border](#adding-border)
      - [Adding margin](#adding-margin)
      - [Adding padding](#adding-padding)
      - [Adding display](#adding-display)
    - [Adding class to HTML element](#adding-class-to-html-element)
    - [Removing class from HTML element](#removing-class-from-html-element)
  - [💻 Exercises](#-exercises)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# Day 21

## Document Object Model (DOM) - Day 1

Le Document Object Model (DOM) est une interface de programmation pour les documents HTML et XML. Il représente la page de manière structurée et permet aux développeurs de manipuler le contenu, la structure et le style des pages web.

### Getting Element

#### Getting elements by tag name

Nous pouvons obtenir des éléments par leur nom de balise en utilisant la méthode `getElementsByTagName`.

```js
const allTitles = document.getElementsByTagName('h1')
console.log(allTitles) // HTMLCollection(4) [h1, h1, h1, h1]
```

#### Getting elements by class name

Nous pouvons obtenir des éléments par leur nom de classe en utilisant la méthode `getElementsByClassName`.

```js
const allTitles = document.getElementsByClassName('title')
console.log(allTitles) // HTMLCollection(4) [h1.title, h1.title, h1.title, h1.title]
```

#### Getting an element by id

Nous pouvons obtenir un élément par son id en utilisant la méthode `getElementById`.

```js
const firstTitle = document.getElementById('first-title')
console.log(firstTitle) // <h1 id="first-title">First Title</h1>
```

### Getting elements by using querySelector methods

#### Getting an element by querySelector

Nous pouvons obtenir un élément en utilisant le sélecteur CSS en utilisant la méthode `querySelector`.

```js
const firstTitle = document.querySelector('#first-title')
console.log(firstTitle) // <h1 id="first-title">First Title</h1>
```

#### Getting elements by querySelectorAll

Nous pouvons obtenir tous les éléments correspondants en utilisant le sélecteur CSS en utilisant la méthode `querySelectorAll`.

```js
const allTitles = document.querySelectorAll('.title')
console.log(allTitles) // NodeList(4) [h1.title, h1.title, h1.title, h1.title]
```

### Adding attribute

Nous pouvons ajouter des attributs à un élément HTML en utilisant la méthode `setAttribute`.

```js
const titles = document.querySelectorAll('h1')
titles.forEach((title, i) => {
  title.setAttribute('id', `title-${i + 1}`)
})
```

### Adding text to HTML element

Nous pouvons ajouter du texte à un élément HTML en utilisant la propriété `textContent`.

```js
const firstTitle = document.querySelector('#first-title')
firstTitle.textContent = 'First Title'
```

### Adding styles to HTML element

#### Adding style color

Nous pouvons ajouter des styles à un élément HTML en utilisant la propriété `style`.

```js
firstTitle.style.color = 'red'
```

#### Adding background color

```js
firstTitle.style.backgroundColor = 'yellow'
```

#### Adding font-size

```js
firstTitle.style.fontSize = '24px'
```

#### Adding border

```js
firstTitle.style.border = '1px solid black'
```

#### Adding margin

```js
firstTitle.style.margin = '10px'
```

#### Adding padding

```js
firstTitle.style.padding = '10px'
```

#### Adding display

```js
firstTitle.style.display = 'block'
```

### Adding class to HTML element

Nous pouvons ajouter des classes à un élément HTML en utilisant la méthode `classList.add`.

```js
firstTitle.classList.add('title', 'header-title')
```

### Removing class from HTML element

Nous pouvons supprimer des classes d'un élément HTML en utilisant la méthode `classList.remove`.

```js
firstTitle.classList.remove('header-title')
```

## 💻 Exercises

### Exercises: Level 1

1. Obtenez l'élément par id.
2. Obtenez les éléments par balise.

### Exercises: Level 2

1. Ajoutez un attribut à un élément.
2. Modifiez le style d'un élément.

### Exercises: Level 3

1. Ajoutez une classe à un élément.
2. Supprimez une classe d'un élément.