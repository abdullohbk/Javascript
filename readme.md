
----- L O O P ----- /////////////////
FOR LOOP /////////
for (initializer; condition; iterator) {
  // statements
}

for (let i = 1; i <= 10; i++) {
  console.log(i);
}

for (let i = 2; i <= 10; i += 2) {
  console.log(i);
}

WITHOUT INITIALIZER ///
let j = 1; // initilizer
for (; j <= 10; j += 1) {
  console.log(j);
}

WITHOUT CONDITION ///
for (let j = 1; ; j += 1) {
  console.log(j);
  if (j > 10) {
    break;
  } // condition
}

WITHOUT ITERATOR ///
for (let j = 1; j <= 10; ) {
  console.log(j);
  j += 1; // iterator
}

WITHOUT ANY EXPRESSION ///
let j = 1; // initilizer
for (;;) {
  if (j <= 10) {
    console.log(j);
  } // condition
  j += 1; // iterator
}

WITHOUT LOOP BODY ///
for (let i = 0; i <= 10; i++, console.log(i));

for (let i = 1; i <= 10; i++) {
  console.log(i);
}

WHILE LOOP ///////////////
while (condition) {
  // code block to be executed
}

let i = 1;
while (i <= 10) {
  console.log(i);
  i++;
}

let count = 1;

while (count <= 10) {
  console.log(count);
  count += 1;
}

DO-WHILE LOOP ////
do {
  statement;
} while (condition);

let i = 11;
do {
  console.log(i);
  i++;
} while (i <= 10);

 SECRET NUMBER GAME //////////////////////////////////////
generate a secret number between 1 and 10
const MIN = 1;
const MAX = 10;

let secretNumber = Math.floor(Math.random() * (MAX - MIN + 1)) + MIN;

let guesses = 0; // for storing the number of guesses
let hint = ''; // for storing hint
let number = 0;
do {
  // get input from user
  let input = prompt(`Please enter a number between ${MIN} and ${MAX}` + hint);

  // get the integer
  number = parseInt(input);

  // increase the number of guesses
  guesses++;

  // check input number with the secret number provide hint if needed
  if (number > secretNumber) {
    hint = ', and less than ' + number;
  } else if (number < secretNumber) {
    hint = ', and greater than ' + number;
  } else if (number == secretNumber) {
    alert(`Bravo! you're correct after ${guesses} guess(es).`);
  }
} while (number != secretNumber);


for (let i = 0; i < 5; i++) {
  console.log(i);
  if (i == 2) {
    break;
  }
}

let i = 0;

while (i < 5) {
  i++;
  console.log(i);
  if (i == 3) {
    break;
  }
}

CONTINUE //////////////////////
for (let i = 1; i <= 10; i++) {
  if (i % 2 !== 0) {
    continue;
  }
  console.log(i);
}

let i = 0;
while (i < 10) {
  i++;
  if (i % 2 === 0) {
    continue;
  }
  console.log(i);
}


7-DARS  //////////////////////////////////////////////////

### switsh - taqoslash operatori

let a = +prompt("Bahoyingizni kiriting");
if(Number.isInteger(a) && a >0 && a < 6){
    switch (a){
        case 1 :
            console.log(`Sizning bahoyingiz(' ${a} ')  yomon `);
            break;
        case 2 :
            console.log(`Sizning bahoyingiz(' ${a} ')  qoniqarsiz `);
            break;
        case 3 :
            console.log(`Sizning bahoyingiz(' ${a} ')  qoniqarli `);
            break;
         case 4 :
            console.log(`Sizning bahoyingiz(' ${a} ')  yahshi `);
            break;
        case 5 :
            console.log(`Sizning bahoyingiz(' ${a} ')  alo `);
            break;   
    }
}else{
    console.log("Xato !");
}


### if else -shartli operator

let a = +prompt("a sonini kiriting");
let b = +prompt("b sonini kiriting");
if (a % 2 == 1 && b % 2 == 1){
    console.log("siz kiritga ikkala son ham tog son");
}else{
    console.log("sizkiritgan sonlar ten tog bo'lishligi kerak")
}

### Global scope

// let a = 3;

// var b = 4;

// const c = 5;

// if (true) {

//   console.log(a);

//   console.log(b);

//   console.log(c);
// }

// switch (a) {

//   case 3:

//     console.log(a);

//     console.log(b);

//     console.log(c);

//     break;
// }


### Local or Function scope

// function add() {

//   let a = 3;

//   var b = 4;

//   const c = 5;

// }

// add();

// console.log(a);

// console.log(b);

// console.log(c);


### For loop

// for (initializer; condition; iterator) {

//   // statements

// }

// for (let i = 1; i <= 10; i++) {

//   console.log(i);

// }

// for (let i = 2; i <= 10; i += 2) {

//   console.log(i);

// }

### While loop

 // while (condition) {

//   // code block to be executed

// }

// let i = 1;

// while (i <= 10) {

//   console.log(i);

//   i++;

// }

// let count = 1;

// while (count <= 10) {

//   console.log(count);

//   count += 1;

// }