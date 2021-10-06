// задание 1

let value = +prompt("Введите значение");

if(typeof value == "number" && !isNaN(value)) {
  console.log(value);
  if(value % 2 == 0){
    console.log("Четное число")
  } else if(value % 2 !== 0) {
    console.log("Нечетное число")
  }
} else {
  alert("Упс, кажется вы ошиблись")
}
  
// задание 2

let x = true;
switch(typeof x) {
  case  'number':
    console.log(x + " - число");
    break;
  case 'string':
    console.log(x + " - строка");
    break;
  case 'boolean':
    console.log(x + " - логический тип");
    break;
  default:
    console.log("Тип "+ x + " не определен");
}

// задание 3

let string = "Строка";
let stringReverse = string.split("").reverse().join("");
console.log(stringReverse);

// задание 4


let num = Math.floor(Math.random() * 101);
console.log(num);


// задание 5

let arr = [1, 2, 3, "string"];
console.log(arr.length);

arr.map(function(item, index, array){
  console.log(item)
});

// задание 6 

let arr = [];

for (i = 1; i < arr.length; i++) {
 if (arr[i - 1] == arr[i]) {
     console.log(true)
   } else {
     console.log(false);
   }
 }

 // задание 7

let arr = [1, 2, 0, 3, 4, 5, 0, 0, 6]
let odd = 0;
let even = 0;
let zero = 0;

for(i = 0; i < arr.length; i++) {
  if(typeof arr[i] === 'number' && !isNaN(arr[i])) {
    if(arr[i] % 2 == 0 && arr[i] !== 0) {
      even++;
    } else if (arr[i] % 2 !== 0 && arr[i] !== 0) {
      odd++;
    } else if (arr[i] == 0) {
      zero++;
    }
  }
}
console.log(`Чётных элементов: ${even}`);
console.log(`Нечетных элементов: ${odd}`);
console.log(`Нулевых элементов: ${zero}`);

//задание 8

let person = new Map([
  ['name', 'Anastasiya'],
  ['age', 30],
  ['height', 160]
]);

for(let [question, answer] of person) {
  console.log(`Ключ - ${question}, значение - ${answer}`);
}