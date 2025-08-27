<script setup>
    import { ref } from 'vue'
    let texto = ref('')

    let nome = ref('') //Isadora
    let email = ref('') //isadora@gmail.com
    let idade = ref('') //17 anos.
    let bio = ref('') //Estudante de Biomedicina.

    let peso = ref('')
    let altura = ref('')
    let imc = ref('')

</script>

<template>
    <p>Valor do input: {{ texto }}</p>
    <input type="text" v-model="texto">

    <p>Nome: {{ nome }}</p>
    <input type="text" v-model="nome">
    <p>Email: {{ email }}</p>
    <input type="text" v-model="email">
    <p>Idade: {{ idade }}</p>
    <input type="text" v-model="idade">
    <p>Bio: {{ bio }}</p>
    <input type="text" v-model="bio">

    <p>Peso: {{ peso }}</p>
    <input type="text" v-model="peso">
    <p>Altura: {{ altura }}</p>
    <input type="text" v-model="altura">
    <p>{{ `IMC: ${peso / (altura * altura)}` }}</p>


</template>

<style scoped>
</style>