# js-intensive-33
# Домашнее задание №4
1) Какие бывают алгоритмы сортировок ?
  Сортировка пузырьком
  Быстрая сортировка
  Сортировка выбором
2) Прочитать про "Операторы и выражения, циклы в JS"
3) Создать объект Person несколькими способами, после создать объект Person2, чтобы в нём были доступны методы объекта Person. Добавить метод logInfo чтоб он был доступен всем объектам.

   function CreatePerson() {
     return {
       logInfo: function() { console.log("logInfo") }
     }
   }

  const **person** = CreatePerson()

  const **person** = new Object({
     logInfo: function() { console.log("logInfo") }
   })

  const **person2** = Object.assign({}, person)

4) Создать класс PersonThree c get и set для поля name и конструктором, сделать класс наследник от класса Person.

  class Person {
    constructor(name) {
      this._name = name
  }

  get name() {
    return this._name
  }

  set name(name) {
    this._name = name
  }
}

class PersonThree extends Person {
  constructor(name) {
    super(name)
  }
}
