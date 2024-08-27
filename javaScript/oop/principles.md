# Принципы ООП

---

## Наследование

Наследование — это возможность порождать один класс от другого с сохранением всех свойств и методов класса-предка, добавляя при необходимости новые свойства и методы.

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    return `${this.name} makes a sound`;
  }
}

class Dog extends Animal {
  constructor(name) {
    super(name);
  }
}
```

## Полиморфизм

Полиморфизм позволяет объектам разных классов обрабатывать вызовы методов по-своему. Это обеспечивает гибкость и возможность работы с объектами разных типов через единый интерфейс.

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    return `${this.name} makes a sound`;
  }
}

class Dog extends Animal {
  speak() {
    return `${this.name} barks`;
  }
}

class Cat extends Animal {
  speak() {
    return `${this.name} meows`;
  }
}

const animals = [new Dog("Buddy"), new Cat("Mittens")];

animals.forEach((animal) => {
  console.log(animal.speak());
});
```

## Инкапсуляция

Инкапсуляция подразумевает сокрытие свойств объекта и предоставление доступа к ним только через методы.

```javascript
class Person {
  #name; // Приватное поле

  constructor(name, age) {
    this.#name = name;
    this.age = age;
  }

  getName() {
    // Публичный метод для доступа к приватному полю
    return this.#name;
  }

  setName(newName) {
    // Публичный метод для изменения приватного поля
    this.#name = newName;
  }
}
```

## Абстракция

Абстракция заключается в выделении основных характеристик объекта. В программировании это означает создание классов, которые описывают объекты с помощью их свойств и методов, скрывая сложность внутренней реализации.

```javascript
class Vehicle {
  constructor(make, model) {
    this.make = make;
    this.model = model;
  }

  startEngine() {
    console.log("Engine started");
  }

  stopEngine() {
    console.log("Engine stopped");
  }

  drive() {
    console.log("Driving...");
  }
}
```

---

- [Что такое статические свойства и методы?](./static.md)
- [Как обозначаются приватные и защищённые методы и свойства? В чём их разница?](./propertydef.md)
- [Вопросы по JavaScript](../javaScript.md)
- [Главное меню](../../README.md)
