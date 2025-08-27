<script setup>
let nomes = ['Isadora', 'Daniel', 'Pedro', 'Duda']
let compras = ['Pão', 'Leite', 'Ovos', 'Frutas']

let produto = [
    {nome: 'Base', preco: '50.48', categoria: 'Maquiagem'},
    {nome: 'Gloss', preco: '80.00', categoria: 'Maquiagem'},
    {nome: 'Shampoo', preco: '25.00', categoria: 'Higiene'},
]

</script>

<template>
<!-- Exercício 03 -->
    <ul>
        <li v-for="nome in nomes"> {{ nome }}</li>
        <!-- <li v-for="(nome, index) in nomes"> {{ index + 1}}. {{ nome }}</li> -->
    </ul>

<!-- Exercício 03.1 -->
    <ul>
        <li v-for="(compra, index) in compras"> {{ index + 1}}. {{ compra }}</li>
    </ul>

<!-- Exercício 03.2 -->
    <div>
        <ul>
            <li v-for="(produtos, index) in produto"> 
                 {{ index + 1}}. {{ produtos.nome }} . {{ produtos.preco }} . {{ produtos.categoria }}</li>
        </ul>
    </div>

</template>

<style scoped>
    /* Exercício 03.1 */
    ul {
    list-style-type: none;
    padding: 0;
        }

</style>