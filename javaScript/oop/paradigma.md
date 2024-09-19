# Парадигмы ООП

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

Один интерфейс может использоваться для управления разными классами

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

Инкапсуляция в программировании сводится к тому, чтобы не давать доступа к важным данным напрямую. Вместо этого мы создаем ограниченный набор методов, с помощью которых можно работать с данными.

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

Cкрытие сложности внутренней реализации.

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

- [Вопросы по JavaScript](../javaScript.md)
