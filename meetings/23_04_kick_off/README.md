# QA-COP Kick Off Meeting - April 2023

## 1. Agenda

- Meet the QA community
- Present project goals and structure
- JavaScript intro
  - Chrome **DevTools** [Console](https://developer.chrome.com/docs/devtools/console/) & [Snippets](https://developer.chrome.com/docs/devtools/javascript/snippets/)
  - Variables
  - [Primitives](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures): Number, String, Boolean, Undefined, Null
  - Objects literals
  - **JSON**
- Q&A

## 2. Code examples

### 2.1 Variables

```javascript
// RECOMMENDATION: USE const AND let
const age = 41; // block scoped; cannot reassign to the variable
age = age + 1; // this will throw

let salary; // block scoped; variable can be reassigned
salary = 2000;
salary = salary + 500;
salary = 'no income';

var isSet = true; // globally/function scoped; variable can be redeclared and reassigned
isSet = false;
```

### 2.1 Primitives

```javascript
const name = 'John';
console.log(name, typeof name);

let age = 30;
console.log(age, typeof age);

let isEmployed = true;
console.log(isEmployed, typeof isEmployed);

let salary;
console.log(salary, typeof salary);

salary = null;
console.log(salary, typeof salary);
```

### 2.1 Object literals

```javascript
const customer = {
  firstName: 'Jane',
  lastName: 'Doe',
  age: 25,
  details: {
    id: 1,
    isActive: true,
  },
};
console.log(JSON.stringify(customer, null, 2));

console.log('Customer name:', customer.firstName, customer.lastName);
console.log('Customer id:', customer.details.id);
console.log('Customer id:', customer['details']['id']);

// update client info
customer.age++;
customer.details.id = 11;

console.log('Updated customer info:', JSON.stringify(customer, null, 2));

// Array
const numbers = [11, 22, 33, 44, 55];
console.log(numbers);
console.log('First number is:', numbers[0]);
console.log('Third number id:', numbers[2]);

const colors = ['red', 'green'];
console.log('Colors:', JSON.stringify(colors, null, 2));

const name = 'Porsche';
const model = '711';
const isDiesel = false;
const engine = {
  capacity: 3000,
  hp: 300,
};

const car = { name, model, isDiesel, engine, colors };
console.log('Car info', JSON.stringify(car, null, 2));
```

## 3. Resources

- [JavaScript Objects](https://javascript.info/object)
