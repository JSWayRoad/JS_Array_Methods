# JS_Array_Methods

**Объекты позволяют нам создавать одну сущность, которая хранит элементы данных по ключам, а массивы – хранить упорядоченные коллекции данных.** 

**Массив** – это особый тип объекта, предназначенный для работы с упорядоченным набором элементов.  
Элементы массива нумеруются, начиная с нуля.  
Массивы расширяют объекты, так как предусматривают специальные методы для работы с  
упорядоченными коллекциями данных, а также свойство length. Но в основе всё равно лежит объект.  

Объявление
```
let arr = new Array();
let arr = [];
```

**свойство length**  
Это свойство,которое возвращает значение  
если строка то, это свойство возвращает количество кодовых значений в строке.  
если массив то , это наибольший цифровой индекс плюс один.

**Статические и динамические  ключи  объекта**  
```
let user = {
```

**Перебор элементов массива**  
Чтобы пройтись по элементам массива:  
for (let i=0; i<arr.length; i++) – работает быстрее всего, совместим со старыми браузерами.  
for (let item of arr) – современный синтаксис только для значений элементов (к индексам нет доступа).  
for (let i in arr) – никогда не используйте для массивов!

**Шпаргалка по методам массива:**

**Для добавления/удаления элементов:**

push (...items) – добавляет элементы в конец,  
pop() – извлекает элемент с конца,  
shift() – извлекает элемент с начала,  
unshift(...items) – добавляет элементы в начало.  
splice(pos, deleteCount, ...items) – начиная с индекса pos, удаляет deleteCount элементов и вставляет items.  
slice(start, end) – создаёт новый массив, копируя в него элементы с позиции start до end (не включая end).  
concat(...items) – возвращает новый массив: копирует все члены текущего массива и добавляет к нему items. Если какой-то из items является массивом, тогда берутся его элементы.

**forEach/map**  
https://medium.com/front-end-weekly/difference-between-map-and-foreach-bcaf8cdd5404

**Для поиска среди элементов:**

indexOf/lastIndexOf(item, pos) – ищет item, начиная с позиции pos, и возвращает его индекс или -1, если ничего не найдено.  
includes(value) – возвращает true, если в массиве имеется элемент value, в противном случае false.  
find/filter(func) – фильтрует элементы через функцию и отдаёт первое/все значения, при прохождении которых через функцию возвращается true.  
findIndex похож на find, но возвращает индекс вместо значения.

**Для перебора элементов:**

forEach(func) – вызывает func для каждого элемента. Ничего не возвращает.

**Для преобразования массива:**

map(func) – создаёт новый массив из результатов вызова func для каждого элемента.  
sort(func) – сортирует массив «на месте», а потом возвращает его.  
reverse() – «на месте» меняет порядок следования элементов на противоположный и возвращает изменённый массив.  
split/join – преобразует строку в массив и обратно.    
reduce(func, initial) – вычисляет одно значение на основе всего массива, вызывая func для каждого элемента и передавая промежуточный результат между вызовами.

Дополнительно:

Array.isArray(arr) проверяет, является ли arr массивом.  
Обратите внимание, что методы sort, reverse и splice изменяют исходный массив.

### методы массивов

https://learn.javascript.ru/array-methods  
https://developer.mozilla.org/ru/docs/Web/JavaScript/Reference/Global_Objects/Array

**What is the Difference Between map() and forEach() in JavaScript?**  
https://medium.com/front-end-weekly/difference-between-map-and-foreach-bcaf8cdd5404

## Псевдомассив

**Итерируемые объекты** – это объекты, которые реализуют метод Symbol.iterator, как было описано выше.
**Псевдомассивы** – это объекты, у которых есть индексы и свойство length, то есть, они выглядят как массивы.  
Они также могут иметь другие свойства и методы, но у них нет встроенных методов массивов  из-за отличий в прототипе.  
Псевдомассив arg поддерживает методы массива

метод Array.from, который принимает итерируемый объект или псевдомассив и делает из него «настоящий» Array.




