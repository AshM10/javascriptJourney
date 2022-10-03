# JavaScript DOM Manipulation Course via FreeCodeCamp

DOM stands for Document Object Model.
It is a programming interface that allows us to create, change, or remove elements from a website document. 

DOM manipulation is when you use JavaScript to add, remove, and modify elements of a website. It is very common in web development.

![Before we begin](https://user-images.githubusercontent.com/89284873/193674590-9da3b9fa-44ea-407e-9d0b-df2f30a540b5.png)

[FreeCodeCamp](https://www.freecodecamp.org/news/javascript-dom-manipulation/)

## Table of contents

- [DOM Fundamentals](#dom-fundamentals)
  - [Links](#links)
  - [What is the DOM?](#what-is-the-dom)
  - [DOM Tree Analogy](#dom-tree-analogy)
  - [Selecting Elements in the DOM](#selecting-elements)
  - [Styling an Element](#styling-elements)
  - [Creating Elements](#creating-elements)
  - [Adding Elements](#adding-elements)
  - [Modify Text](#modify-text)
  - [Modifying Elements Attributes & Classes](#atrritbutes-classes)
  - [Remove an Element](#remove-element)
  - [DOM Tree Recap](#tree-recap)
  - [Traversing the DOM](#traversing-dom)
  - [Event Listeners](#event-listeners)
  - [Event Listener Example](#event-listener-example)
  - [Event Propagation](#event-propagation)
  - [Event Delegation](#event-delegation)
  - [Introduction to Projects](#introduction-to-projects)
- [Project 1: Beginner](#project-1-beginner)
- [Project 2: Beginner Plus](#project-2-beginner-plus)
- [Project 3: Intermediate](#project-3-intermediate)
- [Project 4: Pro ](#project-4-pro)
- [Project 5: Master](#project-5-master)

## DOM Fundamentals 

### What is the DOM?

![What is the DOM](https://user-images.githubusercontent.com/89284873/193674672-f5050bf8-0bce-449f-bec1-2177f461ccc3.png)

### DOM Tree Analogy
Parent-child-sibling Relationship of Nodes

![DOM Tree](https://user-images.githubusercontent.com/89284873/193674765-45b1795c-1a78-4c1c-b64a-a856f11269c3.png)

### Selecting Elements in the DOM

How to select these nodes in the DOM tree for manipulation:

![Favourite Movie Franchise](https://user-images.githubusercontent.com/89284873/193675001-ec4ca9f7-cd3e-440c-8ea8-ed3540629845.png)

Let's take a look at the browser:

![Screen Shot 2022-10-03 at 3 08 18 PM](https://user-images.githubusercontent.com/89284873/193675616-fab6033d-a13b-4513-b464-57d1d79c15b8.png)

#### GetElementById()
- Select this element by its unique ID.
- Place inside a variable so you can manipulate it.

```js
const title = document.getElementById(`main-heading`);
console.log(title);
```

#### GetElementByClassName()
- This method actually returns an array of all the child elements in the given class name (in index and the order that they are in the html file).

```js
const listItems = document.getElementByClassName('list-items');
console.log(listItems);
```

#### GetElementByTagName()
- pretty similar to getElementByClassName() except it returns all elements specified in that tag name. 

```js
const listItems = document.getElementByTagName('li');
console.log(listItems);
```

#### querySelector()
- used to select one item or the first item that matches the selector given.
- can accept all CSS Style selectors

```js
const container = document.querySelector('div');
console.log(container);
```

#### querySelectorAll()
- returns a node list.
- returns all the elements that matches the given selector.

```js
const container = document.querySelectorAll('div');
console.log(container);
```

** Note: Recommended to use: querySelector() and querySelectorAll() **

### Styling an Element

#### Access CSS with JavaScript
- write css variable in camelcase when accessing in JavaScript

```js
const title = document.querySelector('#main-heading');
title.style.color = 'red';
```

![Screen Shot 2022-10-03 at 3 55 34 PM](https://user-images.githubusercontent.com/89284873/193680788-11598d92-f1a7-4a25-b2a4-1328bb77b1d1.png)

```js
const listItems = document.querySelectorAll('list-items');

for (i = 0; i < listItems.length; i++) {
   listItems[i].style.fontSize = '2rem';
}
```

![Screen Shot 2022-10-03 at 3 59 15 PM](https://user-images.githubusercontent.com/89284873/193681387-837d9bbd-f003-48f9-92e0-0e95a8f3d9b5.png)

** Note: listItems will be changes once you loop through the lists. 

### Creating Elements

Stopped video at 16:27.


### Adding Elements
### Modify Text
### Modifying Elements Attributes & Classes
### Remove an Element
### DOM Tree Recap
### Traversing the DOM
### Event Listeners
### Event Listener Example
### Event Propagation
### Event Delegation
### Introduction to Projects

## Project 1: Beginner

- General Styles for All Projects
- Project 1 Mark-Up
- Project 1 CSS Styling
- Project 1 JavaScript

## Project 2: Beginner Plus

- Project 2 Mark Up
- Project 2 CSS styling
- Project 2 JavaScript
- Project 2 CSS Styling p2

## Project 3: Intermediate

- Project 3 Mark Up
- Project 3 CSS Styling
- Project 3 JavaScript
- Project 3 CSS Styling p2

## Project 4: Pro

- Project 4 Mark Up
- Project 4 CSS Styling
- Project 4 JavaScript

## Project 5: Master

- Project 5 Mark Up
- Project 5 CSS Styling
- Project 5 JavaScript
