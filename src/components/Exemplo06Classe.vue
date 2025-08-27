<script setup>
    let validacao = true // false ou true mostram a frase em verde ou vermelho
    let isError = true

    let isDisable = false
    let isActive = true
    

</script>

<template>
    <p :class="validacao ? 'ok' : 'falha'">Utilizando a diretiva class</p> <!--"?" if simplificado, ":" else-->

    <p :class="{
        'ok': isActive, 
        'falha': isError
    }"> Teste Diretiva Class</p>
    <button :disabled="isDisable"> Clique aqui!</button>


    <button :class="{
        'ok': isActive, 
        'falha': isError,
        'validacao': validacao
    }" :disabled="isDisable"> Clique aqui!!</button>

</template>

<style scoped>

.ok {
    color:green
}
.falha {
    color: red
}

.validacao {
    color:black
}

</style>