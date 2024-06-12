<script setup lang="ts">
import { CLIENT_RENEG_LIMIT } from 'tls';

let obj={};
obj = '是是是';
let a:number=4
obj = (a:number) => a +1
console.log(obj,3);
//strictNullChecks设置之后
// let y :null=undefined;//报错
let x :any =undefined;//不报错啊


let c :string|number;
c=4;
c='看看';

//联合类型
function printId(
  id:number|string
) {
  if (typeof id === 'string') {
    console.log(id.toUpperCase());
  } else {
    console.log(id);
  }
}
let d =printId('stjjk')
// console.log(d);
let e:string='设施';
console.log(typeof 'e');
console.log(typeof 23);
//数组
let arr:number[]=[1,2,3]
let arr2:Array<number|string>;
arr2=['设施','让人','数独']
//加入第四位元素
arr2[3]='外网'
//查看第三位元素
console.log(arr2[3]);
//让arr2的长度为2 输出结果就是 ['设施', '让人']
arr2.length=2;
console.log(arr2);

const arr3:readonly number[]=[0,1]
//元祖
const s:[string,boolean,number,number?]=['是谁',true,3]
type t1 =[string,string,...boolean[]];
const f:t1=['额额','确切',true]


</script>

<template>
 111
 
</template>

<style scoped>

</style>
