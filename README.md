# js-intensive-33
# Домашнее задание №5

**1)**
let promiseTwo = new Promise((resolve, reject) => {
   resolve("a");
});

promiseTwo
  .then((res) => {
     return res + "b";
  })
  .then((res) => {
     return res + "с";
  })
  .finally((res) => {
     return res + "!!!!!!!";
  })
  .catch((res) => {
     return res + "d";
  })
  .then((res) => {
     console.log(res); // abc
  });
  Answer: "abc"

**2)**
function doSmth() {
   return Promise.resolve("123");
}

doSmth()
.then(function (a) {
   console.log("1", a); // "1", "123"
   return a; // "123"
})
.then(function (b) {
   console.log("2", b); // "2", "123"
   return Promise.reject("321");
})
.catch(function (err) {
   console.log("3", err); // "3", "321"
})
.then(function (c) {
  console.log("4", c); // "4", undefined
  return c;
});

**3)** Напишите функцию, которая будет проходить через массив целых чисел и выводить индекс каждого элемента с задержкой в 3 секунды.
Входные данные: [10, 12, 15, 21]

function indexTimeout(arr) {
  for (let i = 0; i < arr.length; i++) {
    setTimeout(() => {
      console.log("Индекс", i, ":", arr[i]);
    }, i * 3000);
  }
}

**4)** Прочитать про Top Level Await (можно ли использовать await вне функции async)
  Да, await можно использовать вне функции async, это удобно для инициализации модуля или ожидания результата асинхронной операции до продолжения выполнения кода. Однако не все среды выполнения JS это поддерживают.
