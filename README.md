# js-intensive-33
# Домашнее задание №3

1) Написать ответ - почему массивы в JS являются "неправильными" и совмещают в себе несколько структур данных? Какие ?
Массивы в JS являются "неправильными", потому что:
  1. Массивы могут включать в себе нечисловые ключи
    const arr = [];
    arr["ключ"] = 'элемент по ключу';
    console.log(arr["ключ"]);  // Выведет "элемент по ключу"
  2. В массивах JS можно хранить элементы различных типов данных: строки, числа, объекты и другие массивы.
  3. Массивы в JS предоставляют методы для добавления и удаления элементов, такие как push, pop, shift, unshift, splice, что позволяет им работать как стеки, очереди, hash таблицы.
  4. Массивы в JS наследуют свойства и методы объектов, что позволяет им хранить свойства, а также использовать методы, такие как hasOwnProperty, toString и valueOf.
   
2) Привязать контекст объекта к функции logger, чтобы при вызове this.item выводило - some value (Привязать через bind, call, apply)
  function logger() {
    console.log(`I output only external context: ${this.item}`);
  }
  
  const obj = { item: "some value" };
  
  const boundLogger = logger.bind(obj);
  boundLogger(); // Выведет: "I output only external context: some value"

  logger.call(obj); // Выведет: "I output only external context: some value"
  logger.apply(obj); // Выведет: "I output only external context: some value"


  
Бонус задание: Реализовать полифил(собственную функцию реализующую встроенную в js) метода bind()

Funtion.proptotype.bind = funtion(context){
	const func = this; // Сохраняем ссылку на оригинальную функцию в переменной func
	return function(…args) {  // Возвращаем анонимную функцию, которая будет вызвана с новым контекстом
		return func.apply(
			context,
			args
		);
  }
}
