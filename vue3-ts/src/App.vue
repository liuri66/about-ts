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

</script>

<template>
  333322

</template>

<style scoped>

</style>
