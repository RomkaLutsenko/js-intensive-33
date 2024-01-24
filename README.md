# js-intensive-33
# Домашнее задание №2

Задание 1 – Создать объект counter всеми возможными способами

  const counter = {}  
  const counter = new ByFunctionCounter()  
  const counter = new Counter()  
  const counter = Object.create(null)  
  const counter = Object.create({})  
  const counter = Object.assign({}, counter)  
  
  const ByFunctionCounter() {  
  &ensp;  this.count = 1  
  }  
  class Counter {  
  &ensp;  constructor() {  
  &ensp;&ensp;    this.count = 2  
  &ensp;  }  
  }  
  

Задание 2 – Скопировать объект counter всеми возможными способами  
  const counter = { count: 0 }  
  
  const copiedCounter1 = structuredClone(counter);
  const copiedCounter2 = { ...counter }  
  const copiedCounter3 = Object.assign({}, counter)  
  const copiedCounter4 = JSON.parse(JSON.stringify(counter))  
  const copiedCounter5 = _.cloneDeep(counter)  


Задание 3 – Создать функцию makeCounter всеми описанными и возможными способами  
  const makeCounter = function() {  
  &ensp;  return { count: 0 }  
  }  
  
  function makeCounter() {  
  &ensp;  return { count: 0 }  
  }  
  
  const makeCounter = () => {return { count: 0 }};  

  const makeCounter = function makeCounter(){  
  &ensp;  return { count: 0 }  
  }  

  function MakeCounter() {  
  &ensp;  this.count = 0  
  }  

  (function makeCounter() {  
  &ensp;  return { count: 0 }  
  })()  

Бонус 1 – Написать функцию глубокого сравнения двух объектов:  




















  
