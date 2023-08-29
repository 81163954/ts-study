// interface SquareConfig {
//     width: number,
//     height: number,
//     color: string,
//     [propName: string]: string | number
// }
// interface SearchFunc {
//   (source: {width: number, height: number}, subString: string): boolean;
// }
// let b: SearchFunc = (source: {width: number, height: number}, subString: string) => {
//     return false
// }
// let c: SearchFunc = 1 as unknown as SearchFunc
// b({width: 100, height: 100},"11")
// function addSquare (squareConfig: SquareConfig) : number {
//     return 1
// }
// addSquare({
//     width: 100,
//     height: 200,
//     color: "yellow",
//     id: "1da"
// })


// interface StringArray {
//     [index: number]: string
// }
// let myArray: StringArray = ["bob","coc"]
// let myArray2: String[] = ["bob","coc"]


// interface NumberObject {
//     [index: string]: string
// }
// let numberObject: NumberObject = {
//     name: "bob",
//     age: "two"
// }
// numberObject["age"]


// interface myType {
//     <T>(arg: T): T
// }
// let myFunction1: myType = (arg) => {
// return arg;
// }
// myFunction1<number>(1)


// interface MyType<T> {
//     (arg: T): T
// }
// let myFunction1: MyType<number> = (arg) => {
// return arg;
// }
// myFunction1(1)


// interface myType {
//     length: number
// }
// function myFunction<T extends myType>(arg: T): T {
//     console.log(arg.length)
//     return arg
// }


// enum Enum {
//     A
// }
// let a = Enum.A
// const nameOf = Enum["A"]
// console.log(nameOf)


// interface Named {
//     name: string,
//     // location: string,
// }
// let x: Named
// let y = { name: 'Alice', location: 'Seattle'}
// x = y
