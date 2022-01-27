
```tsx
let myName = "Alice";
myName = 12;

let num = 3 ;


//objects 
let obj: {x: number} = { x: 0 };
obj.y = "12"



type Obj = {
    name: string,

}
let obj2:Obj = {name: "deen"}

let numArray:number[] = [1, 2, 3];


// No type annotations here, but TypeScript can spot the bug
const names = ["Alice", "Bob", "Eve"];
 
// Contextual typing for function
names.forEach(function (s) {
  console.log(s.toUppercase());

});
 
// Contextual typing also applies to arrow functions
names.forEach((s) => {
  console.log(s.toUppercase());

});

// Optional Properties

let newObj:{ first: string; last?: string } = {first: "first" };

// generics 

function test<unknownType>(x:number , y:unknownType):unknownType[] {
 
 return [y];

}

test(1,"4");

let userName = (a:number,b:string) => a+b;
userName(1,2);

// union types 


interface Hero {
    powers : string[],
    heal : () => string ;
}

interface Villain {
    powers : string[];
    burn:() => string ;
}


function test( x : Hero , y:Villain ) {
   console.log(x.powers[0])
   console.log(y.powers[0])

   console.log(x.burn())
   console.log(y.heal())

}

let x:Hero = {
   powers:["x-ray","flight","healing"],
   heal(){ return "heal"}
}

let y:Villain = {
   powers:["burning",""],
   burn(){ return "burn"}
}

test(x ,y)

function testUnion(x : Hero | Villain) {
  x.burn()

  if((x as Hero).heal()) {
     
  }

  if((x as Villain).burn()) {
     
  }
}


// ............................. readonly variables

interface User {
 readonly id: number ,
 name: string
}

const user:User =  {
  id: 1,
  name : "deen"
}

user.id++

// ............................. readonly in class
class User2 {

  readonly id: number ;
  name : string;

  constructor(id: number , name: string){

    this.id = id;
    this.name = name;

  }
}

const user2 = new User2(1 , "deen");
user2.id++ 

// ............................. readonly  array

//mutable - can push to array 

const weekdays1 :string[] = [
  "Sunday",
  "Monday"
]

weekdays1 = ["test"];
weekdays1.push("push");
weekdays1[0] = "test";
 weekdays1.concat("joe");


// readonly [n: number]
const weekdays2 :ReadonlyArray<string> = [
  "Sunday",
  "Monday"
]
   weekdays2[0] = "test";
   weekdays2.push("joe");
  weekdays2.concat("joe");

  // use case

function Test(propArray : ReadonlyArray<number> ){
  propArray.reverse();

}


//Readonly - Does not contain mutable methods vs 

// ReadonlyArray : Any variable with a reference to a ReadonlyArray can’t add, remove, or replace any elements of the array.
// ReadonlyArray : Immutable arrays


// utility types 
// https://www.typescriptlang.org/docs/handbook/utility-types.html

//Enums 

enum Direction {
  Up = 1,
  Down, //2
  Left, //3
  Right,
}

console.log(Direction.Down)

// enum ShirtSize {
//     S = "small",
//     M = "medium",
//     L = "large",
//     XL = "xl"
// }

// objects 

const obj  = {}  // empty object type
// obj.  / no auto complete

// obj.foo = "foo" ;  // not allowed

const obj2: any  = {} 
obj2.a = 2

// functions

function foo(){

  return "a";
}

enum ShirtSize {
    S,
    M,
    L,
    XL
}

function assertNever(value: never): never {
    throw Error(`Unexpected value '${value}'`);
}

function prettyPrint(size: ShirtSize) {
    switch (size) {
        case ShirtSize.S: return "small";
        case ShirtSize.M: return "medium";
        case ShirtSize.L: return "large";
       // case ShirtSize.XL: return "extra large";
        default: return assertNever(size);
    }
}


```