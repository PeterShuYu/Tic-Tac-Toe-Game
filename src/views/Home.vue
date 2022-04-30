<script setup>
let content = $ref('')
let cot = $ref(0)
let k1 = $ref('_,'), k2 = $ref('_,'), k3 = $ref('_'), k4= $ref('_,'), k5 = $ref('_,'), k6 = $ref('_'), k7 = $ref('_,'), k8 = $ref('_,'), k9 = $ref('_')

function check(){
if(cot == 9){content = " TIE "}
if(k1 == k2 & k2 == k3 & k1 != "_,"){content = k1 + " win"}
if(k4 == k5 & k5 == k6 & k4 != "_,"){content = k4 + " win"}
if(k7 == k8 & k8 == k9 & k7 != "_,"){content = k7 + " win"}
if(k1 == k4 & k4 == k7 & k1 != "_,"){content = k1 + " win"}
if(k2 == k5 & k5 == k8 & k2 != "_,"){content = k2 + " win"}
if(k3 == k6 & k6 == k9 & k3 != "_" ){content = k3 + " win"}
if(k1 == k5 & k5 == k9 & k1 != "_,"){content = k1 + " win"}
if(k3 == k5 & k5 == k7 & k3 != "_,"){content = k3 + " win"}
}

function fill_k1(){ k1 = cot%2 ==0 ? "O" : "X"; cot++; check();}
function fill_k2(){ k2 = cot%2 ==0 ? "O" : "X"; cot++; check();}
function fill_k3(){ k3 = cot%2 ==0 ? "O" : "X"; cot++; check();}
function fill_k4(){ k4 = cot%2 ==0 ? "O" : "X"; cot++; check();}
function fill_k5(){ k5 = cot%2 ==0 ? "O" : "X"; cot++; check();}
function fill_k6(){ k6 = cot%2 ==0 ? "O" : "X"; cot++; check();}
function fill_k7(){ k7 = cot%2 ==0 ? "O" : "X"; cot++; check();}
function fill_k8(){ k8 = cot%2 ==0 ? "O" : "X"; cot++; check();}
function fill_k9(){ k9 = cot%2 ==0 ? "O" : "X"; cot++; check();}


</script>

<template>
  <p> Tic-Tac-Toe Game </p>
  <p> RESULT: {{content}} </p>

  <br>
  <button @click="fill_k1">{{k1}}</button>
  <button @click="fill_k2">{{k2}}</button>
  <button @click="fill_k3">{{k3}}</button>
  <br>
  <button @click="fill_k4">{{k4}}</button>
  <button @click="fill_k5">{{k5}}</button>
  <button @click="fill_k6">{{k6}}</button>
  <br>
  <button @click="fill_k7">{{k7}}</button>
  <button @click="fill_k8">{{k8}}</button>
  <button @click="fill_k9">{{k9}}</button>
  <br>
  <br>

  <p @click="k1 = '_,'; k2='_,'; k3='_'; k4 = '_,'; k5='_,'; k6='_'; k7 = '_,'; k8='_,'; k9='_';cot = 0; content = ''">RESET</p>
</template>

<style scoped>
input { background: #eee; }
</style>
