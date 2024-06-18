<script setup lang="ts">
let foo:string='zhjj';
console.log(foo);
let a :num;
a=5;
console.log(a);
let b:any;
b=1;
b='zhlr';
b=true;

let c:symblo=Symbol();
// const d:unique symblo=Symbol();
const d:unique symbol = Symbol();

//函数
function fun1(params:string) {
  // 函数体
  console.log('参数类型是'+params);
}
fun1('文字');
//函数赋值给一个变量
const e = function (params2:string) {
  // 函数体
  console.log('参数类型是'+params2);
};
e('文字2');

const f :
(params:string) => void
=function (params3) {
  console.log('参数类型是'+params3);
  
}
f('文字3')
//箭头函数
const repeat =(
  str:string,
  times:number
):string => str.repeat(times)
function f3(params?:number) {
  return x;
};
f();
f(10);
function f2():void {
  console.log('22');
}
//构造函数
 const d2 =new Date();
//对象
const obj1:{
  g:number;
  h:number,
} = {g:1,h:2}

type obj2={
  x:number;
  y:number;
}

const i:obj2 ={x:1,y:2}
console.log(i.x); 
const obj3:{
  x:number;
  y:number;
  add(x:number,y:number):number;
}={
  x:1,y:2,add(x,y){
    return x +y;
  }
}
const obj4:{} ={};
let obj5:{};
let obj6:Object;
obj5 ={x:1};
obj5 ='hello';
//接口
interface Person{
  firstName:string;
  lastName:string;
  age:number;
}

const p:Person={
  firstName: 'John',
  lastName: 'Smith',
  age: 25
}
console.log(p.age);
type A = Person['age']
// console.log(A);
//属性索引
interface Myobj{
  [prop:string]:number;//属性索引指定所有名称为字符串的属性，它们的属性值必须是数值
  // a:12;
}
//数值索引
interface Aa {
  [prop: number]: string;
}
const obj:A =['A','B','C']
//接口方法
interface A1 {
 f(x:string):string;
}
interface A2 {
  f:(x:boolean) => string;
}
interface A3 {
  f:{(x:boolean):string}
}
//接口函数
interface Add {
  (x:number,y:number): number;
}
const myAdd:Add = (x,y) => x +y; //接口Add声明了一个函数类型。
//构造函数
interface A4 {
  new (message?: string) :Error;
}
//接口继承
interface Shape {
  name: string;
};

interface Circle extends Shape {
  radius: number;
};
class A5 {
  x :string='';
  y():boolean{
    return true;
  }
}
interface A6 extends A5{
  z: number
};
const A7:A6={
  x:'', //A5的
  y:function(){
    return true;
  },//A5的
  z:23, //A6的
}
interface Box {
  height: number;
  width: number;
}

interface Box {
  length: number;
};
const A8:Box={
  height:4,
  length:54,
  width:6,
}
console.log(A8.height);
//类
class C{
  _name='foo';
  get name (){
    return this._name;
  }
}
const c1 =new C();

class D {
  [s:string]:boolean|
  ((s:string)=> boolean);
  get (s:string ){
    return this[s] as boolean
  }
}
interface Point{
  x:number;
  y:number;
}
class MyPoint implements Point{
  x=1;
  y=2;
  z:number =1;
}
//class类型
class color {
  name:string;
  constructor(name:string){
    this.name =name;
  }
}
const blue:color =new color('blue')
function createColor(
  ColorClass:typeof color,
  name:string
):color {
  return new ColorClass(name);
}
//
class Foo{
  id!:number;
}
function fn(arg:Foo) {
  
}
const bar={
  id:1,
  amount:100,
};
fn(bar)
//
class bot{
  protected x ='保护的成员';
}
class bing extends bot{
  getX(){
    return this.x
  }
}
const B =new bing()

console.log(B.getX());

class th{
  name='a'
}
//Enum 类型
enum color1 {
  red,
  blue,
}
let  color2 =color1.blue
console.log(color2);
//
const p1:{x:number}={x:1,y:1} as {x:number;y:number}
//断言函数
function isString(value:unknown):asserts value is string {
  if (typeof value !== 'string')
  throw new Error('Not a string');
}
type AccessLevel = 'r' | 'w' | 'rw';

function allowsReadAccess(
  level:AccessLevel
):asserts level is 'r' | 'rw' {
  if (!level.includes('r'))
    throw new Error('Read not allowed');
}
allowsReadAccess('r')
console.log(allowsReadAccess);
// console.log(allowsReadAccess('r'));
// 对象类型Person2
type Person2 ={
  name:string;
  email?:string;
}
//loadPerson2函数，没有参数，返回值是Person2或者null null可以赋值给任意类型
function loadPerson2():Person2 | null {
  return null;
}
//loadPerson2函数赋值给person2
let person2 =loadPerson2();

function assert(
  // unknown，可以赋值为各种类型的值
  condition: unknown,
  message: string
  //判断condition参数 断言函数的asserts语句等同于void类型，
  // 所以如果返回除了undefined和null以外的值，都会报错
):asserts condition {
  // !非空断言操作符
  if (!condition) throw new Error(message);
}

// person2是任意类型不是非空，就是输出错误
assert(person2,'Person2 is not defined')
console.log(person2.name);
</script>

<template>
  333322

</template>

<style scoped>

</style>
