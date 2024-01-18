
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


8-DARS///////////////////////////////////////////////////////

### Mavzu: Funcsiya , funcsiyanig asosiy 3 ta turi :

- Function declaration

- Function expession

- Arrow function


### 1. F U N C T I O N S


Funksiya - JavaScript dasturlash tilining asoslaridan biri bo'lob uning yordamida malum bir vazifani bajarish mumkun . Funksiya boshqa bir kod qismida chaqirilganda ishga tushadi . Funksiya yordamida kodni qayta ishlatishlik imkoni mavjud yani birmarotaba elon qilib , bir necha joyda ishlatishlik imkoni mavjud , o'hshati lozim bo'lsa SCSS degi mixsend larga qisman o'hshab ketadi.

- Sintactisti quydagicha :
```

function square(number) {
 return number * number;
}



function power(a,n){
    let b = a**n;
    return b
}

console.log(power(3,2));

// natija ==> 9 


```


### Function declaration
Funktsiya deklaratsiyasi nima? Funktsiya deklaratsiyasi funktsiyani belgilaydigan identifikatorni kiritadi va ixtiyoriy ravishda funktsiya parametrlarining turlarini (prototipi) belgilaydi. Funktsiya e'lonlari (ta'riflardan farqli o'laroq) fayllar ko'lami bilan bir qatorda blok doirasida ham paydo bo'lishi mumkin.

Funktsiya declaration qolganlaridan yanabir kuchli farqi uni elon qilib olganimazdan so'ng istalgan joyda chaqirib ishlata olamiz hatto funksiya elongqilingan satirdan yuqorida chaqirib ham !

```


function sonBoluvch(n) {
    for (let i = 1 ; i < n ; i++) {
        if(n % i == 0){
            console.log(i);
        }
    }
}
sonBoluvch(10);



```

### Function expession
Function expession sintaksis jihatdan huddi declaration ohshaydi , asosiy farq bu funksiya nomi bo‘lib yani declarationda biz funcsiyaga nim bergan bo'lsak bunda o'zgaruvchi elon qilib unga funcsiyani elon qilib ketamiz va chaqirib olishda shu o'zgaruvchi nomi bilan chaqirib olamiz , yana bir asosiy farqi uni o'zidan yoqorida chaqira olmaymiz !

Function expession afzalig jihatilaridan biri shuki unu yan ihtiyori bir ozgaruvchiga tenglab , ihtiyoricha o'zlashtirib ishlatishligimiz mumkun , buni 2- misolda ko'rsak yanayam tushunarliroq bo'ladi !

```

const funcNam = function () {
    console.log("Lesson - 8");
}

funcNam(); // natija ==>  Lesson - 8

// -------------- 2 - misol -----------------

const funcNam = function (a , b) {
    console.log(a+b);
}

funcNam(4,6); // natiga ==> 10

let test = funcNam ;

test(20,67); // ===>  87 


```

### Arrow function
Arrow function hozirgacha ko'rgan funcsiyalarimiz ichida va umumiy jihatda eng ko'p ishlatladigan funcsiya bo'lib hisoblanadi u ishlash jihatidan avalgi korganlarimiz bilan birhiln ish bajaradi sintacsistida biroz far qiladi unin misolda ko'rsak yanayam tushunarliroq bo'ladi.

Arrow function yana bir avzalligi uni stentminti birdona bo'ladigan bo'lsa uni hechqanday bloc skoplarsiz yan " { } " yai figurni qavuslarsiz bir qatorning o'zida yozib ketsak ham boladi 1- misolda ko'rishligimiz mumkun


```


// ---------  1- misol  -------

const funcNam = () => console.log("hello");

funcNam(); // natija ===> hello

// -------- 2 misol--------------------------

const funcNam = (a, b , c) => {
    if(a>b && b>c){
        console.log(a+b/c);
    }else{
        console.log(a+b+c);
    }
};

funcNam(20,12,4); // natija ==> 23



```
