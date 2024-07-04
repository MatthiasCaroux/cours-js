<div align="center">
  <h1> 30 Days Of JavaScript: Types de Données</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/asabeneh/">
  <img src="https://img.shields.io/badge/style--5eba00.svg?label=LinkedIn&logo=linkedin&style=social">
  </a>
  <a class="header-badge" target="_blank" href="https://twitter.com/Asabeneh">
  <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/asabeneh?style=social">
  </a>

  <sub>Auteur :
  <a href="https://www.linkedin.com/in/asabeneh/" target="_blank">Asabeneh Yetayeh</a><br>
  <small> Janvier 2020</small>
  </sub>
</div>
</div>

[<< Jour 1](../readMe.md) | [Jour 3 >>](../03_Day_Booleans_operators_date/03_booleans_operators_date.md)

![Thirty Days Of JavaScript](../images/banners/day_1_2.png)

- [📔 Jour 2](#-jour-2)
  - [Types de Données](#types-de-données)
    - [Types de Données Primitives](#types-de-données-primitives)
    - [Types de Données Non-Primitives](#types-de-données-non-primitives)
      - [Longues Chaînes Littérales](#longues-chaînes-littérales)
      - [Séquences d'Échappement dans les Chaînes](#séquences-déchappement-dans-les-chaînes)
      - [Littéraux de Gabarits (Template Strings)](#littéraux-de-gabarits-template-strings)
    - [Méthodes de Chaînes](#méthodes-de-chaînes)
  - [Vérification des Types de Données et Conversion](#vérification-des-types-de-données-et-conversion)
    - [Vérification des Types de Données](#vérification-des-types-de-données)
    - [Changement de Type de Données (Conversion)](#changement-de-type-de-données-conversion)
      - [Chaîne en Entier](#chaîne-en-entier)
      - [Chaîne en Flottant](#chaîne-en-flottant)
      - [Flottant en Entier](#flottant-en-entier)
  - [💻 Jour 2 : Exercices](#-jour-2--exercices)
    - [Exercice : Niveau 1](#exercice--niveau-1)
    - [Exercice : Niveau 2](#exercice--niveau-2)
    - [Exercices : Niveau 3](#exercices--niveau-3)

# 📔 Jour 2

## Types de Données

Dans la section précédente, nous avons mentionné brièvement les types de données. Les données ou les valeurs ont des types de données. Les types de données décrivent les caractéristiques des données. Les types de données peuvent être divisés en deux catégories :

1. Types de données primitifs
2. Types de données non-primitifs (Références d'Objets)

### Types de Données Primitives

Les types de données primitifs en JavaScript comprennent :

 1. Nombres - Entiers, nombres à virgule flottante
 2. Chaînes de caractères - Toute donnée entre guillemets simples, guillemets doubles ou guillemets inversés
 3. Booléens - Valeur vraie ou fausse
 4. Null - Valeur vide ou aucune valeur
 5. Undefined - une variable déclarée sans valeur
 6. Symbole - Une valeur unique qui peut être générée par le constructeur Symbol

Les types de données non-primitifs en JavaScript incluent :

1. Objets
2. Tableaux

Voyons maintenant ce que signifient exactement les types de données primitifs et non-primitifs.
*Les types de données primitifs* sont immuables (non modifiables). Une fois qu'un type de données primitif est créé, nous ne pouvons pas le modifier.

**Exemple:**

```js
let mot = 'JavaScript'
```

Si nous essayons de modifier la chaîne stockée dans la variable *mot*, JavaScript devrait générer une erreur. Toute donnée sous guillemets simples, guillemets doubles ou guillemets inversés est un type de données de chaîne.

```js
mot[0] = 'Y'
```

Cette expression ne modifie pas la chaîne stockée dans la variable *mot*. Ainsi, nous pouvons dire que les chaînes ne sont pas modifiables ou, en d'autres termes, immuables.
Les types de données primitifs sont comparés par leurs valeurs. Voyons un exemple de comparaison de différentes valeurs de données :

```js
let numUn = 3
let numDeux = 3

console.log(numUn == numDeux)      // true

let js = 'JavaScript'
let py = 'Python'

console.log(js == py)             // false 

let allume = true
let eteint = false

console.log(allume == eteint) // false
```

### Types de Données Non-Primitives

*Les types de données non-primitifs* sont modifiables. Nous pouvons modifier la valeur des types de données non-primitifs après leur création.
Voyons cela en créant un tableau. Un tableau est une liste de valeurs de données entre crochets. Les tableaux peuvent contenir des types de données identiques ou différents. Les valeurs du tableau sont référencées par leur index. En JavaScript, l'index du tableau commence à zéro. Par exemple, le premier élément d'un tableau se trouve à l'index zéro, le deuxième élément à l'index un, et le troisième élément à l'index deux, etc.

```js
let nums = [1, 2, 3]
nums[0] = 10

console.log(nums)  // [10, 2, 3]
```

Comme vous pouvez le voir, un tableau, qui est un type de données non-primitif, est mutable. Les types de données non-primitifs ne peuvent pas être comparés par valeur. Même si deux types de données non-primitifs ont les mêmes propriétés et valeurs, ils ne sont pas strictement égaux.

```js
let nums = [1, 2, 3]
let numbers = [1, 2, 3]

console.log(nums == numbers)  // false

let utilisateurUn = {
nom:'Asabeneh',
role:'enseignement',
pays:'Finlande'
}

let utilisateurDeux = {
nom:'Asabeneh',
role:'enseignement',
pays:'Finlande'
}

console.log(utilisateurUn == utilisateurDeux) // false
```

En règle générale, nous ne comparons pas les types de données non-primitifs. Ne comparez pas les tableaux, les fonctions ou les objets.
Les valeurs non-primitives sont appelées types de référence, car elles sont comparées par référence au lieu de par valeur. Deux objets ne sont strictement égaux que s'ils font référence au même objet sous-jacent.

```js
let nums = [1, 2, 3]
let numbers = nums

console.log(nums == numbers)  // true
```
```markdown
```js
```markdown
Concaténer en utilisant l'opérateur d'addition est une méthode ancienne. Cette façon de concaténer est fastidieuse et sujette aux erreurs. Il est bon de savoir comment concaténer de cette manière, mais je vous recommande fortement d'utiliser les chaînes de gabarits ES6 (expliquées plus tard).

```js
// Déclaration de différentes variables de différents types de données
let space = ' '
let firstName = 'Asabeneh'
let lastName = 'Yetayeh'
let country = 'Finland'
let city = 'Helsinki'
let language = 'JavaScript'
let job = 'teacher'
let age = 250

let fullName = firstName + space + lastName
let personInfoOne = fullName + '. I am ' + age + '. I live in ' + country; // Ajout de chaîne de caractères ES5

console.log(personInfoOne)
```

```sh
Asabeneh Yetayeh. I am 250. I live in Finland
```

#### Longues Chaînes Littérales

Une chaîne de caractères peut être un seul caractère, un paragraphe ou une page. Si la longueur de la chaîne est trop grande, elle ne tient pas sur une ligne. Nous pouvons utiliser le caractère antislash (\\) à la fin de chaque ligne pour indiquer que la chaîne continuera sur la ligne suivante.
**Exemple:**

```js
const paragraph = "My name is Asabeneh Yetayeh. I live in Finland, Helsinki.\
I am a teacher and I love teaching. I teach HTML, CSS, JavaScript, React, Redux, \
Node.js, Python, Data Analysis and D3.js for anyone who is interested to learn. \
In the end of 2019, I was thinking to expand my teaching and to reach \
to global audience and I started a Python challenge from November 20 - December 19.\
It was one of the most rewarding and inspiring experience.\
Now, we are in 2020. I am enjoying preparing the 30DaysOfJavaScript challenge and \
I hope you are enjoying too."

console.log(paragraph)
```

#### Séquences d'Échappement dans les Chaînes

En JavaScript et dans d'autres langages de programmation, \ suivi de certains caractères est une séquence d'échappement. Voyons les caractères d'échappement les plus courants :

- \n : nouvelle ligne
- \t : Tabulation, équivaut à 8 espaces
- \\\\ : Antislash
- \\': Guillemets simples (')
- \\": Guillemets doubles (")

```js
console.log('I hope everyone is enjoying the 30 Days Of JavaScript challenge.\nDo you ?') // saut de ligne
console.log('Days\tTopics\tExercises')
console.log('Day 1\t3\t5')
console.log('Day 2\t3\t5')
console.log('Day 3\t3\t5')
console.log('Day 4\t3\t5')
console.log('This is a backslash  symbol (\\)') // Pour écrire un antislash
console.log('In every programming language it starts with \"Hello, World!\"')
console.log("In every programming language it starts with \'Hello, World!\'")
console.log('The saying \'Seeing is Believing\' isn\'t correct in 2020')
```

Sortie dans la console :

```sh
I hope everyone is enjoying the 30 Days Of JavaScript challenge.
Do you ?
Days  Topics  Exercises
Day 1 3 5
Day 2 3 5
Day 3 3 5
Day 4 3 5
This is a backslash  symbol (\)
In every programming language it starts with "Hello, World!"
In every programming language it starts with 'Hello, World!'
The saying 'Seeing is Believing' isn't correct in 2020
```

#### Littéraux de Gabarits (Template Strings)

Pour créer des chaînes de gabarits, nous utilisons deux backticks. Nous pouvons injecter des données sous forme d'expressions dans une chaîne de gabarits. Pour injecter des données, nous entourons l'expression avec des accolades ({}) précédées d'un signe $ . Voir la syntaxe ci-dessous.

```js
//Syntaxe
`String literal text`
`String literal text ${expression}`
```

**Exemple: 1**

```js
console.log(`The sum of 2 and 3 is 5`)              // écrire les données statiquement
let a = 2
let b = 3
console.log(`The sum of ${a} and ${b} is ${a + b}`) // injecter les données dynamiquement
```

**Exemple:2**

```js
let firstName = 'Asabeneh'
let lastName = 'Yetayeh'
let country = 'Finland'
let city = 'Helsinki'
let language = 'JavaScript'
let job = 'teacher'
let age = 250
let fullName = firstName + ' ' + lastName

let personInfoTwo = `I am ${fullName}. I am ${age}. I live in ${country}.` //ES6 - Méthode d'interpolation de chaîne
let personInfoThree = `I am ${fullName}. I live in ${city}, ${country}. I am a ${job}. I teach ${language}.`
console.log(personInfoTwo)
console.log(personInfoThree)
```

```sh
I am Asabeneh Yetayeh. I am 250. I live in Finland.
I am Asabeneh Yetayeh. I live in Helsinki, Finland. I am a teacher. I teach JavaScript.
```

En utilisant un gabarit de chaîne ou une méthode d'interpolation de chaîne, nous pouvons ajouter des expressions, qui pourraient être une valeur ou certaines opérations (comparaison, opérations arithmétiques, opération ternaire).

```js
let a = 2
let b = 3
console.log(`${a} is greater than ${b}: ${a > b}`)
```

```sh
2 is greater than 3: false
```

### Méthodes de Chaînes

Tout en JavaScript est un objet. Une chaîne de caractères est un type de donnée primitif, ce qui signifie que nous ne pouvons pas la modifier une fois créée. L'objet chaîne a de nombreuses méthodes de chaîne. Il existe différentes méthodes de chaîne qui peuvent nous aider à travailler avec des chaînes.

1. *length* : La méthode *length* de la chaîne retourne le nombre de caractères dans une chaîne, y compris les espaces vides.

**Exemple:**

```js
let js = 'JavaScript'
console.log(js.length)         // 10
let firstName = 'Asabeneh'
console.log(firstName.length)  // 8
```

2. *Accéder aux caractères d'une chaîne* : Nous pouvons accéder à chaque caractère d'une chaîne en utilisant son index. En programmation, le comptage commence à 0. Le premier index de la chaîne est zéro, et le dernier index est la longueur de la chaîne moins un.

  ![Accéder à la chaîne par index](../images/string_indexes.png)
  
Accédons à différents caractères de la chaîne 'JavaScript'.

```js
let string = 'JavaScript'
let firstLetter = string[0]

console.log(firstLetter)           // J

let secondLetter = string[1]       // a
let thirdLetter = string[2]
let lastLetter = string[9]

console.log(lastLetter)            // t

let lastIndex = string.length - 1

console.log(lastIndex)  // 9
console.log(string[lastIndex])    // t
```

3. *toUpperCase()* : Cette méthode change la chaîne en lettres majuscules.

```js
let string = 'JavaScript'

console.log(string.toUpperCase())     // JAVASCRIPT

let firstName = 'Asabeneh'

console.log(firstName.toUpperCase())  // ASABENEH

let country = 'Finland'

console.log(country.toUpperCase())    // FINLAND
```

4. *toLowerCase()* : Cette méthode change la chaîne en lettres minuscules.

```js
let string = 'JavasCript'

console.log(string.toLowerCase())     // javascript

let firstName = 'Asabeneh'

console.log(firstName.toLowerCase())  // asabeneh

let country = 'Finland'

console.log(country.toLowerCase())   // finland
```

5. *substr()* : Elle prend deux arguments, l'index de départ et le nombre de caractères à extraire.

```js
let string = 'JavaScript'
console.log(string.substr(4,6))    // Script

let country = 'Finland'
console.log(country.substr(3, 4))   // land
```

6. *substring()* : Elle prend deux arguments, l'index de départ et l'index de fin mais elle n'inclut pas le caractère à l'index de fin.

```js
let string = 'JavaScript'

console.log(string.substring(0,4))     // Java
console.log(string.substring(4,10))    // Script
console.log(string.substring(4))       // Script

let country = 'Finland'

console.log(country.substring(0, 3))   // Fin
console.log(country.substring(3, 7))   // land
console.log(country.substring(3))      // land
```

7. *split()* : La méthode split divise une chaîne à un endroit spécifié.

```js
let string = '

30 Days Of JavaScript'

console.log(string.split())     // Change en tableau -> ["30 Days Of JavaScript"]
console.log(string.split(' '))  // Divise en tableau à chaque espace -> ["30", "Days", "Of", "JavaScript"]

let firstName = 'Asabeneh'

console.log(firstName.split())    // Change en tableau - > ["Asabeneh"]
console.log(firstName.split(''))  // Divise en tableau à chaque lettre ->  ["A", "s", "a", "b", "e", "n", "e", "h"]

let countries = 'Finland, Sweden, Norway, Denmark, and Iceland'

console.log(countries.split(','))  // divise en tableau à chaque virgule -> ["Finland", " Sweden", " Norway", " Denmark", " and Iceland"]
console.log(countries.split(', ')) //  ["Finland", "Sweden", "Norway", "Denmark", "and Iceland"]
```

8. *trim()* : Supprime les espaces en début et en fin de chaîne.

```js
let string = '   30 Days Of JavaScript   '

console.log(string)
console.log(string.trim(' '))

let firstName = ' Asabeneh '

console.log(firstName)
console.log(firstName.trim())  // supprime toujours les espaces en début et en fin de chaîne
```

```sh
   30 Days Of JavaScript   
30 Days Of JavaScript
  Asabeneh 
Asabeneh
```

9. *includes()* : Elle prend un argument sous-chaîne et vérifie si cet argument existe dans la chaîne. *includes()* retourne un booléen. Si la sous-chaîne existe dans une chaîne, elle retourne true, sinon elle retourne false.

```js
let string = '30 Days Of JavaScript'

console.log(string.includes('Days'))     // true
console.log(string.includes('days'))     // false - sensible à la casse !
console.log(string.includes('Script'))   // true
console.log(string.includes('script'))   // false
console.log(string.includes('java'))     // false
console.log(string.includes('Java'))     // true

let country = 'Finland'

console.log(country.includes('fin'))     // false
console.log(country.includes('Fin'))     // true
console.log(country.includes('land'))    // true
console.log(country.includes('Land'))    // false
```

10. *replace()* : prend en paramètre l'ancienne sous-chaîne et une nouvelle sous-chaîne.

```js
string.replace(oldsubstring, newsubstring)
```

```js
let string = '30 Days Of JavaScript'
console.log(string.replace('JavaScript', 'Python')) // 30 Days Of Python

let country = 'Finland'
console.log(country.replace('Fin', 'Noman'))       // Nomanland
```

11. *charAt()* : Prend un index et retourne la valeur à cet index

```js
string.charAt(index)
```

```js
let string = '30 Days Of JavaScript'
console.log(string.charAt(0))        // 3

let lastIndex = string.length - 1
console.log(string.charAt(lastIndex)) // t
```

12. *charCodeAt()* : Prend un index et retourne le code ASCII de la valeur à cet index

```js
string.charCodeAt(index)
```

```js
let string = '30 Days Of JavaScript'
console.log(string.charCodeAt(3))        // D le code ASCII est 68

let lastIndex = string.length - 1
console.log(string.charCodeAt(lastIndex)) // t le code ASCII est 116

```

13.  *indexOf()* : Prend une sous-chaîne et si la sous-chaîne existe dans une chaîne, elle retourne la première position de la sous-chaîne, sinon elle retourne -1

```js
string.indexOf(substring)
```

```js
let string = '30 Days Of JavaScript'

console.log(string.indexOf('D'))          // 3
console.log(string.indexOf('Days'))       // 3
console.log(string.indexOf('days'))       // -1
console.log(string.indexOf('a'))          // 4
console.log(string.indexOf('JavaScript')) // 11
console.log(string.indexOf('Script'))     //15
console.log(string.indexOf('script'))     // -1
```

14.  *lastIndexOf()* : Prend une sous-chaîne et si la sous-chaîne existe dans une chaîne, elle retourne la dernière position de la sous-chaîne, sinon elle retourne -1

```js
//syntax
string.lastIndexOf(substring)
```

```js
let string = 'I love JavaScript. If you do not love JavaScript what else can you love.'

console.log(string.lastIndexOf('love'))       // 67
console.log(string.lastIndexOf('you'))        // 63
console.log(string.lastIndexOf('JavaScript')) // 38
```

15. *concat()* : elle prend plusieurs sous-chaînes et les joint.

```js
string.concat(substring, substring, substring)
```

```js
let string = '30'
console.log(string.concat("Days", "Of", "JavaScript")) // 30DaysOfJavaScript

let country = 'Fin'
console.log(country.concat("land")) // Finland
```

16. *startsWith* : elle prend une sous-chaîne comme argument et vérifie si la chaîne commence par cette sous-chaîne spécifiée. Elle retourne un booléen (true ou false).

```js
//syntax
string.startsWith(substring)
```

```js
let string = 'Love is the best to in this world'

console.log(string.startsWith('Love'))   // true
console.log(string.startsWith('love'))   // false
console.log(string.startsWith('world'))  // false

let country = 'Finland'

console.log(country.startsWith('Fin'))   // true
console.log(country.startsWith('fin'))   // false
console.log(country.startsWith('land'))  //  false
```

17. *endsWith* : elle prend une sous-chaîne comme argument et vérifie si la chaîne se termine par cette sous-chaîne spécifiée. Elle retourne un booléen (true ou false).

```js
string.endsWith(substring)
```

```js
let string = 'Love is the most powerful feeling in the world'

console.log(string.endsWith('world'))         // true
console.log(string.endsWith('love'))          // false
console.log(string.endsWith('in the world')) // true

let country = 'Finland'

console.log(country.endsWith('land'))         // true
console.log(country.endsWith('fin'))          // false
console.log(country.endsWith('Fin'))          //  false
```

18. *search* : elle prend une sous-chaîne comme argument et retourne l'index de la première correspondance. La valeur de recherche peut être une chaîne ou un modèle d'expression régulière.

```js
string.search(substring)
```

```js
let string = 'I love JavaScript. If you do not love JavaScript what else can you love.'
console.log(string.search('love'))          // 2
console.log(string.search(/javascript/gi))  // 7
```

19. *match* : elle prend une sous-chaîne ou un modèle d'expression régulière comme argument et retourne un tableau s'il y a une correspondance, sinon elle retourne null. Voyons à quoi ressemble un modèle d'expression régulière. Il commence par le signe / et se termine par le signe /.

```js
let string = 'love'
let patternOne = /love/     // sans aucun drapeau
let patternTwo = /love/gi   // g signifie rechercher dans tout le texte, i - insensible à la casse
```

Syntaxe de match

```js
// syntaxe
string.match(substring)
```

```js
let string = 'I love JavaScript. If you do not love JavaScript what else can you love.'
console.log(string.match('love'))
```

```sh
["love", index: 2, input: "I love JavaScript. If you do not love JavaScript what else can you love.", groups: undefined]
```

```js
let pattern = /love/gi
console.log(string.match(pattern))   // ["love", "love", "love"]
```

Extrayons des nombres du texte en utilisant une expression régulière. Ce n'est pas la section des expressions régulières, ne paniquez pas ! Nous aborderons les expressions régulières plus tard.

```js
let txt = 'In 2019, I ran 30 Days of Python. Now, in 2020 I am super exited to start this challenge'
let regEx = /\d+/

// d avec un caractère d'échappement signifie d pas un d normal mais agit comme un chiffre
// + signifie un ou plusieurs nombres de chiffres,
// s'il y a un g après, cela signifie global, rechercher partout.

console.log(txt.match(regEx))  // ["2", "0", "1", "9", "3", "0", "2", "0", "2", "0"]
console.log(txt.match(/\d+/g)) // ["2019", "30", "2020"]
```

20. *repeat()* : elle prend un nombre comme argument et retourne la version répétée de la chaîne.

```js
string.repeat(n)
```

```js
let string = 'love'
console.log(string.repeat(10)) // lovelovelovelovelovelovelovelovelovelove
```



## Vérification des Types de Données et Conversion

### Vérification des Types de Données

Pour vérifier le type de données d'une certaine variable, nous utilisons la méthode _typeof_.

**Exemple:**

```js
// Différents types de données JavaScript
// Déclarons différents types de données

let firstName = 'Asabeneh'      // chaîne de caractères
let lastName = 'Yetayeh'        // chaîne de caractères
let country = 'Finland'         // chaîne de caractères
let city = 'Helsinki'           // chaîne de caractères
let age = 250                   // nombre, ce n'est pas mon âge réel, ne vous inquiétez pas
let job                         // undefined, car une valeur n'a pas été assignée

console.log(typeof 'Asabeneh')  // chaîne de caractères
console.log(typeof firstName)   // chaîne de caractères
console.log(typeof 10)          // nombre
console.log(typeof 3.14)        // nombre
console.log(typeof true)        // booléen
console.log(typeof false)       // booléen
console.log(typeof NaN)         // nombre
console.log(typeof job)         // undefined
console.log(typeof undefined)   // undefined
console.log(typeof null)        // objet
```

### Changement de Type de Données (Conversion)

- Conversion : Convertir un type de données en un autre type de données. Nous utilisons _parseInt()_, _parseFloat()_, _Number()_, _+ signe_, _str()_
  Lorsque nous faisons des opérations arithmétiques, les nombres de chaînes doivent d'abord être convertis en entier ou en flottant, sinon cela retourne une erreur.

#### Chaîne en Entier

Nous pouvons convertir un nombre de chaîne en un nombre. Tout nombre à l'intérieur de guillemets est un nombre de chaîne. Un exemple de nombre de chaîne : '10', '5', etc.
Nous pouvons convertir une chaîne en nombre en utilisant les méthodes suivantes :

- parseInt()
- Number()
- Plus sign(+)

```js
let num = '10'
let numInt = parseInt(num)
console.log(numInt) // 10
```

```js
let num = '10'
let numInt = Number(num)

console.log(numInt) // 10
```

```js
let num = '10'
let numInt = +num

console.log(numInt) // 10
```

#### Chaîne en Flottant

Nous pouvons convertir un nombre flottant de chaîne en un nombre flottant. Tout nombre flottant à l'intérieur de guillemets est un nombre flottant de chaîne. Un exemple de nombre flottant de chaîne : '9.81', '3.14', '1.44', etc.
Nous pouvons convertir un nombre flottant de chaîne en nombre en utilisant les méthodes suivantes :

- parseFloat()
- Number()
- Plus sign(+)

```js
let num = '9.81'
let numFloat = parseFloat(num)

console.log(numFloat) // 9.81
```

```js
let num = '9.81'
let numFloat = Number(num)

console.log(numFloat) // 9.81
```

```js
let num = '9.81'
let numFloat = +num

console.log(numFloat) // 9.81
```

#### Flottant en Entier

Nous pouvons convertir des nombres flottants en entiers.
Nous utilisons la méthode suivante pour convertir un flottant en entier :

- parseInt()
  
```js
let num = 9.81
let numInt = parseInt(num)

console.log(numInt) // 9
```

🌕  Vous êtes incroyable. Vous venez de terminer les défis du jour 2 et vous êtes deux pas plus près de la grandeur. Maintenant, faites quelques exercices pour votre cerveau et vos muscles.  

## 💻 Jour 2 : Exercices

### Exercice : Niveau 1

1. Déclarez une variable nommée challenge et assignez-lui une valeur initiale **'30 Days Of JavaScript'**.
2. Affichez la chaîne dans la console du navigateur en utilisant __console.log()__
3. Affichez la __longueur__ de la chaîne dans la console du navigateur en utilisant _console.log()_
4. Changez tous les caractères de la chaîne en majuscules en utilisant la méthode __toUpperCase()__
5. Changez tous les caractères de la chaîne en minuscules en utilisant la méthode __toLowerCase()__
6. Coupez (slice) le premier mot de la chaîne en utilisant la méthode __substr()__ ou __substring()__
7. Coupez la phrase *Days Of JavaScript* de *30 Days Of JavaScript*.
8. Vérifiez si la chaîne contient le mot __Script__ en utilisant la méthode __includes()__
9. Divisez la __chaîne__ en __tableau__ en utilisant la méthode __split()__
10. Divisez la chaîne 30 Days Of JavaScript à l'espace en utilisant la méthode __split()__
11. 'Facebook, Google, Microsoft, Apple, IBM, Oracle, Amazon' __divisez__ la chaîne à la virgule et changez-la en tableau.
12. Changez 30 Days Of JavaScript en 30 Days Of Python en utilisant la méthode __replace()__.
13. Quel est le caractère à l'index 15 dans la chaîne '30 Days Of JavaScript' ? Utilisez la méthode __charAt()__.
14. Quel est le code de caractère de J dans la chaîne '30 Days Of JavaScript' en utilisant __charCodeAt()__
15. Utilisez __indexOf__ pour déterminer la position de la première occurrence de __a__ dans 30 Days Of JavaScript
16. Utilisez __lastIndexOf__ pour déterminer la position de la dernière occurrence de __a__ dans 30 Days Of JavaScript.
17. Utilisez __indexOf__ pour trouver la position de la première occurrence du mot __because__ dans la phrase suivante :__'You cannot end a sentence with because because because is a conjunction'__
18. Utilisez __lastIndexOf__ pour trouver la position de la dernière occurrence du mot __because__ dans la phrase suivante :__'You cannot end a sentence with because because because is a conjunction'__
19. Utilisez __search__ pour trouver la position de la première occurrence du mot __because__ dans la phrase suivante :__'You cannot end a sentence with because because because is a conjunction'__
20. Utilisez __trim()__ pour supprimer tout espace en début et en fin de chaîne. Par exemple ' 30 Days Of JavaScript '.
21. Utilisez la méthode __startsWith()__ avec la chaîne *30 Days Of JavaScript* et faites en sorte que le résultat soit true
22. Utilisez la méthode __endsWith()__ avec la chaîne *30 Days Of JavaScript* et faites en sorte que le résultat soit true
23. Utilisez la méthode __match()__ pour trouver tous les __a__ dans 30 Days Of JavaScript
24. Utilisez __concat()__ et fusionnez '30 Days of' et 'JavaScript' en une seule chaîne, '30 Days Of JavaScript'
25. Utilisez la méthode __repeat()__ pour afficher 30 Days Of JavaScript 2 fois

### Exercice : Niveau 2

1. En utilisant console.log() affichez l'énoncé suivant :

    ```sh
    The quote 'There is no exercise better for the heart than reaching down and lifting people up.' by John Holmes teaches us to help one another.
    ```

2. En utilisant console.log() affichez la citation suivante de Mère Teresa :

    ```sh
    "Love is not patronizing and charity isn't about pity, it is about love. Charity and love are the same -- with charity you give love, so don't just give money but reach out your hand instead."
    ```

3. Vérifiez si le type de '10' est exactement égal à 10. Sinon, faites en sorte qu'il soit exactement égal.
4. Vérifiez si parseFloat('9.8') est égal à 10. Sinon, faites en sorte qu'il soit exactement égal à 10.
5. Vérifiez si 'on' se trouve à la fois dans python et jargon
6. _I hope this course is not full of jargon_. Vérifiez si _jargon_ est dans la phrase.
7. Générez un nombre aléatoire entre 0 et 100 inclusivement.
8. Générez un nombre aléatoire entre 50 et 100 inclusivement.
9. Générez un nombre aléatoire entre 0 et 255 inclusivement.
10. Accédez aux caractères de la chaîne 'JavaScript' en utilisant un nombre aléatoire.
11. Utilisez console.log() et des caractères d'échappement pour afficher le modèle suivant.

    ```js
    1 1 1 1 1
    2 1 2 4 8
    3 1 3 9 27
    4 1 4 16 64
    5 1 5 25 125
    ```

12. Utilisez __substr__ pour extraire la phrase __because because because__ de la phrase suivante :__'You cannot end a sentence with because because because is a conjunction'__

### Exercices : Niveau 3

1. 'Love is the best thing in this world. Some found their love and some are still looking for their love.' Comptez le nombre de mots __love__ dans cette phrase.
2. Utilisez __match()__ pour compter le nombre de tous les __because__ dans la phrase suivante :

__'You cannot end a sentence with because because because is a conjunction'__
3. Nettoyez le texte suivant et trouvez le mot le plus fréquent (indice : utilisez replace et les expressions régulières).

    ```js
        const sentence = '%I $am@% a %tea@cher%, &and& I lo%#ve %te@a@ching%;. The@re $is no@th@ing; &as& mo@re rewarding as educa@ting &and& @emp%o@weri@ng peo@ple. ;I found tea@ching m%o@re interesting tha@n any ot#her %jo@bs. %Do@es thi%s mo@tiv#ate yo@u to be a tea@cher!? %Th#is 30#Days&OfJavaScript &is al@so $the $resu@lt of &love& of tea&ching'
    ```

4. Calculez le revenu annuel total de la personne en extrayant les chiffres du texte suivant. 'He earns 5000 euro from salary per month, 10000 euro annual bonus, 15000 euro online courses per month.'

🎉 FÉLICITATIONS ! 🎉

[<< Jour 1](../readMe.md) | [Jour 3 >>](../03_Day_Booleans_operators_date/03_booleans_operators_date.md)
```