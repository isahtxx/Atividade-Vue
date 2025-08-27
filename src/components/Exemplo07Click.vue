<script setup>
    function mensagem(){
        alert('Trabalhando com eventos de cliques')
    }

    import { ref } from 'vue'
    const contador = ref(0)
    const estado = ref('ativo')

    function incrementar() {
    contador.value++
    }
    function decrementar(){
        if(contador.value > 0){
            contador.value--
        }
    }
    function resetar(){
        contador.value = 0
    }
    function alterarEstado(){
        estado.value = estado.value === 'ativo'
    }

</script>

<template>
    <button @click="mensagem"> Clique aqui!</button>

    <div>
        <p> Contador: {{ contador }}</p>
        <p>Estado: {{ estado }}</p>
        <button @click="decrementar" :disable="contador === 0" || estado != 'ativo'> Decrementar </button>
        <button @click="incrementar" :disable="contador === 0" || estado != 'ativo'> Incrementar </button>
        <button @click="resetar" :disable="contador === 0" || estado != 'ativo'> Resetar </button>

    </div>

</template>

<style scoped>

</style>