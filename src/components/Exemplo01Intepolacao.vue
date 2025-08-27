<script setup>
let nomee = 'Daniel'
let num1 = 20
let num2 = 20

let nome = 'Isadora'
let idade = 17
let profissao = 'Biomedicina'

let a = 15
let b = 25

let data = new Date() .getFullYear()

</script>

<template>
    <p>{{ `Meu nome é: ${nomee}`}}</p>
    <p>{{ num1 + num2 }}</p>

    <p>{{ `Meu nome é: ${nome}, tenho ${idade}, e sou ${profissao}`}}</p>

    <p>{{ `Adiçaõ: ${a + b}` }}</p>
    <p>{{ `Subtração: ${a - b}` }}</p>
    <p>{{ `Multiplicação: ${a * b}` }}</p>
    <p>{{ `Divisão: ${a / b}` }}</p>

    <p>{{ `A data atual é: ${data}` }}</p>

</template>