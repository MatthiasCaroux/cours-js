<div align="center">
  <h1> 30 Days Of JavaScript: Event Listeners</h1>
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

[<< Day 22](../22_Day_Manipulating_DOM_object/22_day_manipulating_DOM_object.md) | [Day 24 >>](../24_Day_Project_solar_system/24_day_project_solar_system.md)

![Thirty Days Of JavaScript](../images/banners/day_1_23.png)

- [Day 22](#day-22)
  - [DOM(Document Object Model)-Day 3](#domdocument-object-model-day-3)
    - [Event Listeners](#event-listeners)
      - [Click](#click)
      - [Double Click](#double-click)
      - [Mouse Enter](#mouse-enter)
      - [Mouse Leave](#mouse-leave)
      - [Mouse Over](#mouse-over)
      - [Mouse Out](#mouse-out)
      - [Key Press](#key-press)
      - [Key Down](#key-down)
      - [Key Up](#key-up)
      - [Input Event](#input-event)
      - [Blur Event](#blur-event)
      - [Change Event](#change-event)
  - [💻 Exercises](#-exercises)
    - [Exercises: Level 1](#exercises-level-1)
    - [Exercises: Level 2](#exercises-level-2)
    - [Exercises: Level 3](#exercises-level-3)

# Day 22

## DOM(Document Object Model)-Day 3

### Event Listeners

Les écouteurs d'événements (event listeners) sont utilisés pour exécuter du code JavaScript lorsqu'un événement se produit. Voici quelques exemples d'écouteurs d'événements courants.

#### Click

```js
const button = document.querySelector('button')
button.addEventListener('click', () => {
  alert('Button clicked')
})
```

#### Double Click

```js
const button = document.querySelector('button')
button.addEventListener('dblclick', () => {
  alert('Button double clicked')
})
```

#### Mouse Enter

```js
const div = document.querySelector('div')
div.addEventListener('mouseenter', () => {
  div.style.backgroundColor = 'lightblue'
})
```

#### Mouse Leave

```js
const div = document.querySelector('div')
div.addEventListener('mouseleave', () => {
  div.style.backgroundColor = ''
})
```

#### Mouse Over

```js
const div = document.querySelector('div')
div.addEventListener('mouseover', () => {
  div.style.border = '1px solid black'
})
```

#### Mouse Out

```js
const div = document.querySelector('div')
div.addEventListener('mouseout', () => {
  div.style.border = ''
})
```

#### Key Press

```js
document.addEventListener('keypress', (event) => {
  console.log(`Key pressed: ${event.key}`)
})
```

#### Key Down

```js
document.addEventListener('keydown', (event) => {
  console.log(`Key down: ${event.key}`)
})
```

#### Key Up

```js
document.addEventListener('keyup', (event) => {
  console.log(`Key up: ${event.key}`)
})
```

#### Input Event

```js
const input = document.querySelector('input')
input.addEventListener('input', (event) => {
  console.log(`Input value: ${event.target.value}`)
})
```

#### Blur Event

```js
const input = document.querySelector('input')
input.addEventListener('blur', () => {
  console.log('Input lost focus')
})
```

#### Change Event

```js
const select = document.querySelector('select')
select.addEventListener('change', (event) => {
  console.log(`Selected value: ${event.target.value}`)
})
```

## 💻 Exercises

### Exercises: Level 1

1. Ajoutez un écouteur d'événement de clic à un bouton et affichez une alerte lorsque le bouton est cliqué.
2. Ajoutez un écouteur d'événement de double clic à un bouton et affichez une alerte lorsque le bouton est double cliqué.

### Exercises: Level 2

1. Ajoutez un écouteur d'événement de survol (mouseover) à un div et modifiez sa couleur de fond lorsqu'il est survolé.
2. Ajoutez un écouteur d'événement de sortie de survol (mouseout) à un div et réinitialisez sa couleur de fond lorsqu'il n'est plus survolé.

### Exercises: Level 3

1. Ajoutez un écouteur d'événement de pression de touche (keypress) à l'ensemble du document et affichez la touche pressée dans la console.
2. Ajoutez un écouteur d'événement de changement (change) à une liste déroulante (select) et affichez la valeur sélectionnée dans la console.