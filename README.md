```typescript
interface SquareConfig {
    width: number,
    height: number,
    color: string,
    [propName: string]: string | number
}
interface SearchFunc {
  (source: {width: number, height: number}, subString: string): boolean;
}
let b: SearchFunc = (source: {width: number, height: number}, subString: string) => {
    return false
}
let c: SearchFunc = 1 as unknown as SearchFunc
b({width: 100, height: 100},"11")
function addSquare (squareConfig: SquareConfig) : number {
    return 1
}
addSquare({
    width: 100,
    height: 200,
    color: "yellow",
    id: "1da"
})


interface StringArray {
    [index: number]: string
}
let myArray: StringArray = ["bob","coc"]
let myArray2: String[] = ["bob","coc"]


interface NumberObject {
    [index: string]: string
}
let numberObject: NumberObject = {
    name: "bob",
    age: "two"
}
numberObject["age"]


interface myType {
    <T>(arg: T): T
}
let myFunction1: myType = (arg) => {
return arg;
}
myFunction1<number>(1)


interface MyType<T> {
    (arg: T): T
}
let myFunction1: MyType<number> = (arg) => {
return arg;
}
myFunction1(1)


interface myType {
    length: number
}
function myFunction<T extends myType>(arg: T): T {
    console.log(arg.length)
    return arg
}


enum Enum {
    A
}
let a = Enum.A
const nameOf = Enum["A"]
console.log(nameOf)


interface Named {
    name: string,
    // location: string,
}
let x: Named
let y = { name: 'Alice', location: 'Seattle'}
x = y


const date = new Date()
date.setFullYear(2001)
date.toTimeString()
console.log(date.toTimeString())


let identity = function<T>(x: T): T {
    return x
}
let reverse = function<U>(y: U): U {
    return y
}
identity = reverse  // y: any -> x: any


interface Bird {
    fly(): void
    layEggs(): void
}
interface Fish {
    swim(): void
    layEggs(): void
}
function getSmallPet(): Bird | Fish {
    let a: any
    return a as Bird | Fish
}
let pet = getSmallPet()
pet.layEggs()
if((pet as Bird).fly) {
    (pet as Bird).fly()
} else {
    (pet as Fish).swim()
}
function isBird(pet: Fish | Bird): pet is Bird {
    return (pet as Bird).fly !== undefined
}
if(isBird(pet)){
    pet.fly()
} else {
    pet.swim()
}




interface Padder {
    getPaddingString(): string
}

class SpaceRepeatingPadder implements Padder {
    constructor(private numSpaces: number) { }
    getPaddingString(): string {
        console.log("SpaceRepeatingPadder")
        return Array(this.numSpaces + 1).join(" ");
    }
}

class StringPadder implements Padder {
    constructor(private value: string) {}
    getPaddingString(): string {
        console.log("StringPadder")
        return this.value
    }
}

function getRandomPadder() {
    return Math.random() < 0.5 ?
        new SpaceRepeatingPadder(4) :
        new StringPadder("  ")
}

let padder: Padder = getRandomPadder()

padder.getPaddingString()

if(padder instanceof SpaceRepeatingPadder) {
    padder.getPaddingString()
}
if(padder instanceof StringPadder) {
    padder.getPaddingString()
}


function fixed(name: string | null): string {
  function postfix(epithet: string) {
    return name!.charAt(0) + '.  the ' + epithet; // ok
  }
  name = name || "Bob";
  return postfix("great");
}


interface Container<T> {
    value: T
}

type Container1<T> = { value: T }

type LinkedList<T> = T & { next: LinkedList<T> };

type DoubleLinkedList<T> = T & { next: LinkedList<T>, previous: LinkedList<T> };

let list: DoubleLinkedList<string>


let sym = Symbol("Nike")
let sym2 = Symbol("Nike")
console.log(sym.valueOf())
console.log(sym.toString())
console.log(sym2.valueOf())
console.log(sym2.toString())



```
