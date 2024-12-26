![](https://codeforgeek.com/wp-content/uploads/2023/07/Object-Mapping-in-JS.png)
1. Что такое объект в JavaScript?
   
Объект — это коллекция пар "ключ-значение", где ключи (или свойства) — это строки, а значения могут быть любыми типами данных (строки, числа, массивы, функции и даже другие объекты).
пример:

const person = {
  name: "John",
  age: 30,
  greet: function() {
    console.log("Hello!");
  }
};

2. Создание объектов
   
С помощью литерала:

const person = { name: "John", age: 30 };


С помощью конструктора new Object():

const person = new Object();
person.name = "John";
person.age = 30;

3. Доступ к свойствам объекта
Через точку:

console.log(person.name);

console.log(person["age"]);  

4. Изменение свойств объекта
Прямое присваивание:

person.name = "Alice";

Используя квадратные скобки:

person["age"] = 35;

5. Ключевые методы работы с объектами
Object.keys(): возвращает массив ключей объекта.

console.log(Object.keys(person)); // ['name', 'greet']

Object.values(): возвращает массив значений объекта

console.log(Object.values(person)); // ['John', function]

Object.entries(): возвращает массив пар [ключ, значение].

console.log(Object.entries(person)); // [['name', 'John'], ['greet', function]]

8. Сравнение объектов
   
Сравнивать объекты напрямую с помощью оператора == или === нельзя, так как они всегда ссылаются на разные участки памяти.

const obj1 = { name: "John" };
const obj2 = { name: "John" };
console.log(obj1 === obj2);  // false

9. Расширенные возможности:
Деструктуризация объекта:

const person = { name: "John", age: 30 };
const { name, age } = person;
console.log(name);  // John
console.log(age);   // 30

10. Методы объектов
Объекты могут содержать не только данные, но и функции, которые называют методами:

const person = {
  name: "John",
  greet: function() {
    console.log(`Hello, my name is ${this.name}`);
  }
};
person.greet();  // Hello, my name is John
![](https://datasagar.com/illionso_awesome/2023/12/JavaScript-Object-Methods.png)
