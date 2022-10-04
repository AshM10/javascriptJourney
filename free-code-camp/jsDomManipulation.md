# JavaScript DOM Manipulation Course via FreeCodeCamp

This repository is made for note-taking about the course. 

DOM stands for Document Object Model.
It is a programming interface that allows us to create, change, or remove elements from a website document. 

DOM manipulation is when you use JavaScript to add, remove, and modify elements of a website. It is very common in web development.

![Before we begin](https://user-images.githubusercontent.com/89284873/193674590-9da3b9fa-44ea-407e-9d0b-df2f30a540b5.png)

[FreeCodeCamp](https://www.freecodecamp.org/news/javascript-dom-manipulation/)

## Table of contents

- [DOM Fundamentals](#dom-fundamentals)
  - [What is the DOM?](#what-is-the-dom)
  - [DOM Tree Analogy](#dom-tree-analogy)
  - [Selecting Elements in the DOM](#selecting-elements-in-the-dom)
  - [Styling an Element](#styling-an-element)
  - [Creating Elements](#creating-elements)
  - [Adding Elements](#adding-elements)
  - [Modify Text](#modify-text)
  - [Modifying Elements Attributes & Classes](#modifying-elements-attritbutes-&-classes)
  - [Remove an Element](#remove-an-element)
  - [DOM Tree Recap](#dom-tree-recap)
  - [Traversing the DOM](#traversing-the-dom)
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

** Note: listItems will be changed once you loop through the lists. 

### Creating Elements

- create a new element by using the createElement method.

```js
const ul = document.querySelector('ul');
const li = document.createElement('li');
```

### Adding Elements

- use the append method to insert (add) the document.

```js
const ul = document.querySelector('ul');
const li = document.createElement('li');

ul.append(li);
```

### Modify Text

- Let's add a span inside the html:
  
![Screen Shot 2022-10-04 at 12 26 23 PM](https://user-images.githubusercontent.com/89284873/193886159-4e645848-8a58-4195-a22e-4df6a8c9921c.png)

- Ways to target an element:

```js
const firstListItem = document.querySelector('.list-items');

console.log(firstListItem.innerText);
console.log(firstListItem.textContent);
console.log(firstListItem.innerHTML);
```

![Screen Shot 2022-10-04 at 12 31 41 PM](https://user-images.githubusercontent.com/89284873/193887088-e0935437-d539-41ca-a32d-dd2c674b3f8c.png)

![Screen Shot 2022-10-04 at 12 30 48 PM](https://user-images.githubusercontent.com/89284873/193886931-528b0136-dd8a-4e78-841d-650ced9be17b.png)

** Note: In most cases, just use .innerText because using .innerHTML has a bit of risk to it. **

- Modify text using .innerText

```js
const ul = document.querySelector('ul');
const li = document.createElement('li');

ul.append(li);
li.innerText = 'x-men';
```

### Modifying Elements Attributes & Classes

- Set Attribute method
  - You need to include two values: the attribute you want to set, the name you want to give that attribute.

```js
li.setAttribute('id', 'main-heading');
```

![Screen Shot 2022-10-04 at 12 40 22 PM](https://user-images.githubusercontent.com/89284873/193888730-951e11d3-e0e6-4a87-85e6-d02d4a4c9c3b.png)

- Removing an attribute

```js
li.setAttribute('id', 'main-heading');
li.removeAttribute('id');
```

![Screen Shot 2022-10-04 at 12 42 17 PM](https://user-images.githubusercontent.com/89284873/193889090-34168586-bc54-4969-83c6-64d630f42ef0.png)

- Access styling attribute

```js
const title = document.querySelector('#main-heading);

console.log(title.getAttribute('id'));
```

![Screen Shot 2022-10-04 at 12 46 56 PM](https://user-images.githubusercontent.com/89284873/193889885-b728f2a3-18be-48f5-8554-db9ac81ec65b.png)

- Add method for classes

```js
li.classList.add('list-items');
```

![Screen Shot 2022-10-04 at 12 48 43 PM](https://user-images.githubusercontent.com/89284873/193890203-4e02e948-4990-4945-8beb-824c75cc5b2e.png)

- removing a class

```js
li.classList.remove('list-items');
```

![Screen Shot 2022-10-04 at 12 49 38 PM](https://user-images.githubusercontent.com/89284873/193890359-d77b332f-3b07-4933-acb9-547e45998cd8.png)

- Find out whether an element has that specific class

```js
console.log(li.classList.contains('list-items'));
```

![Screen Shot 2022-10-04 at 12 51 00 PM](https://user-images.githubusercontent.com/89284873/193890591-82a85fed-0c46-4307-be5d-7ca79f4cc9a6.png)

** Note: console is returning false because we removed the class earlier. **

### Remove an Element

- All we need is the remove method

```js
li.remove();
```

![Screen Shot 2022-10-04 at 12 52 56 PM](https://user-images.githubusercontent.com/89284873/193890940-7c994436-3d43-4e04-bbc5-579d080f3cd0.png)

### DOM Tree Recap

![Screen Shot 2022-10-04 at 12 53 53 PM](https://user-images.githubusercontent.com/89284873/193891138-344fdfe3-e398-4e9b-a926-d1c493506fec.png)

- The DOM object itself is actually a property of the window object.
  - Window object is the global, top object. 
- Document node is the root node. It has one child called the HTML node.
- Class Attributes are also nodes but they don't participate in the parent-child-relationship building. They are considered properties.
- Learning how to traverse a DOM tree is essential to understanding JavaScript and HTML.

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
