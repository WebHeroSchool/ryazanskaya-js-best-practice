# JavaScript Best Practice

## Деструктуризация

1. При обращении к нескольким свойствам объекта используйте деструктуризацию объекта.

👎 **плохо**
``` js
function getFullName(user) {
  const firstName = user.firstName;
  const lastName = user.lastName;

  return `${firstName} ${lastName}`;
}
```
👍 **хорошо**
``` js
function getFullName(user) {
  const { firstName, lastName } = user;
  return `${firstName} ${lastName}`;
}
```
🙌 **отлично**
``` js
function getFullName({ firstName, lastName }) {
  return `${firstName} ${lastName}`;
}
```

## Блоки

1. Используйте фигурные скобки `{}`, когда блок кода занимает несколько строк.

👎 **плохо**
``` js
if (test)
  return false;

function foo() { return false; }
```
👍 **хорошо**
``` js
if (test) return false;

if (test) {
  return false;
}

function bar() {
  return false;
}
```
2. Если блоки кода в условии `if` и `else` занимают несколько строк, расположите оператор `else` на той же строке, где находится закрывающая фигурная скобка блока `if`.

👎 **плохо**
``` js
if (test) {
  thing1();
  thing2();
}
else {
  thing3();
}
```
👍 **хорошо**
``` js
if (test) {
  thing1();
  thing2();
} else {
  thing3();
}
```
## Пробелы

1. Ставьте 1 пробел перед открывающей фигурной скобкой у блока. 

👎 **плохо**
``` js
function test(){
  console.log('test');
}
```
👍 **хорошо**
``` js
function test() {
  console.log('test');
}
```
2. Ставьте 1 пробел перед открывающей круглой скобкой в операторах управления (`if`, `while` и т.п.). Не оставляйте пробелов между списком аргументов и названием в объявлениях и вызовах функций.

👎 **плохо**
``` js
if(isRunner) {
  run ();
}

function run () {
  console.log ('Start!');
}
```
👍 **хорошо**
``` js
if (isRunner) {
  run();
}

function run() {
  console.log('Start!');
}
```
3. Разделяйте операторы пробелами.

👎 **плохо**
``` js
const x=y+5;
```
👍 **хорошо**
``` js
const x = y + 5;
```
4. Оставляйте пустую строку между блоком кода и следующей инструкцией.

👎 **плохо**
``` js
if (foo) {
  return bar;
}
return baz;
```
👍 **хорошо**
``` js
if (foo) {
  return bar;
}

return baz;
```
5. Не добавляйте пробелы между круглыми скобками и их содержимым.

👎 **плохо**
``` js
function bar( foo ) {
  return foo;
}

if ( foo ) {
  console.log(foo);
}
```
👍 **хорошо**
``` js
function bar(foo) {
  return foo;
}

if (foo) {
  console.log(foo);
}
```
6. Добавляйте пробелы между фигурными скобками и их содержимым.

👎 **плохо**
``` js
const user = {name: 'Sam'};
```
👍 **хорошо**
``` js
const user = { name: 'Sam' };
```
7. Начинайте все комментарии с пробела.

👎 **плохо**
``` js
//это текущая вкладка
const active = true;
```
👍 **хорошо**
``` js
// это текущая вкладка
const active = true;
```


## Запятые

1. Не начинайте строку с запятой.

👎 **плохо**
``` js
const hero = {
    firstName: 'Johnny'
  , lastName: 'Depp'
  , birthYear: 1984
};
```
👍 **хорошо**
``` js
const hero = {
  firstName: 'Johnny',
  lastName: 'Depp',
  birthYear: 1984,
};
```

2. Добавляйте висячие запятые после последнего свойства в объектах и массивах.

👎 **плохо**
``` js
const hero = {
  firstName: 'Johnny',
  lastName: 'Depp',
  birthYear: 1984
};
```
👍 **хорошо**
``` js
const hero = {
  firstName: 'Johnny',
  lastName: 'Depp',
  birthYear: 1984,
};
```

## Точка с запятой 

1. Точка с запятой должна присутствовать после каждого выражения.

👎 **плохо**
``` js
const someItem = 'some string'  
function doSomething() {  
  return 'something'  
}  
```
👍 **хорошо**
``` js
const someItem = 'some string';  
function doSomething() {  
  return 'something';  
}  
```
