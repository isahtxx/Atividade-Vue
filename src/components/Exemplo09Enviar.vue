<script setup>

function validaFormulario(event){
    alert('Formulário enviado com sucesso!')

    event.preventDefault()
}
</script>

<template>
    <form action="https://g1.globo.com" @submit=""validaFormulario>
        <input type="subimit" value="Enviar Formulário"></input>
    </form>

</template>