<script setup>
import {ref} from 'vue'
    

let inputValue = ref('')
function mensagem(){
    alert(`Executando a função: ${inputValue.value}`)
}

let keyDown = ref('')
function down(){
    alert(`Testando KeyDown: ${keyDown.value}`)
}
let keyPress = ref('')
function press(){
    alert(`Testando KeyPress: ${keyPress.value}`)
}

</script>

<template>
    <input type="text" @keyup.enter="mensagem" v-model="inputValue"></input>
    <br></br>

    <input type="text" @keydown="down" v-model="keyDown"> </input>
    <br></br>

    <input type="text" @keypress="press" v-model="keyPress"> </input>
    </input>

</template>