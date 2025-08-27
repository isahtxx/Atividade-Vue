<script setup>
// import exercicio01 from './components/Exemplo1Interpolacao.vue'
// import exercicio02 from './components/Exemplo2Condicional.vue'
// import exercicio03 from './components/Exemplo3For.vue'
// import exercicio04 from './components/Exemplo04Html.vue'
// import exercicio05 from './components/Exemplo05Model.vue'
// import exercicio06 from './components/Exemplo06Classe.vue'
// import exercicio07 from './components/Exemplo07Click.vue'
// import exercicio08 from './components/Exemplo08Teclado.vue'
// import exercicio09 from './components/Exemplo09Enviar.vue'

// import UserCard from './components/Exemplo10Props.vue'
// const user = {
//     nome: String,
//     email: String,
//     idade: Number,
//     telefone: String,
//     ativo: Boolean
// }

// import UserCard from './components/ProductCard.vue'

// import {ref} from 'vue'
// import Exemplo11Emits from './components/Exemplo11Emits.vue';
// const totalCliques = ref(0)
// function atualizarTotal(valor){
//     totalCliques.value = valor
// }

import { ref } from "vue"
import UserCard from './components/ExercicioEmits.vue'
const mensagem = ref("")
function adicionarNaLista(produto) {
  mensagem.value = `Item comprado: ${produto}`
}


</script>

<template>
    <!-- <exercicio01></exercicio01> -->
    <!-- <exercicio02></exercicio02> -->
    <!-- <exercicio03></exercicio03> -->
    <!-- <exercicio04></exercicio04> -->
    <!-- <exercicio05></exercicio05> -->
    <!-- <exercicio06></exercicio06> -->
    <!-- <exercicio07></exercicio07> -->
    <!-- <exercicio08></exercicio08> -->
    <!-- <exercicio09></exercicio09> -->

    <!-- <UserCard 
        nome="Isadora" 
        email="isadora@gmail" 
        idade="17" 
        telefone="12345678919" 
        :ativo="true"> 
    </UserCard> -->

    <!-- <UserCard 
        title="Almofada" 
        price="R$ 572,77" 
        image="https://http2.mlstatic.com/D_NQ_NP_2X_725176-MLA87652864645_072025-F.webp"
        :inStock="true"> 
    </UserCard> -->

    <!-- <Exemplo11Emits></Exemplo11Emits>
    <p>Total de cliques: {{ totalCliques }}</p> -->


    <h2>Lista de Compras:</h2>
    <p v-if="mensagem">{{ mensagem }}</p>

    <div class="produtos">
        <UserCard 
        title="Poltrona Branca" 
        price="R$ 572,77" 
        image="https://http2.mlstatic.com/D_NQ_NP_2X_725176-MLA87652864645_072025-F.webp"
        :inStock="true"
        @comprar="adicionarNaLista"
    />
    <UserCard 
      title="Kit Peças Banheiro" 
      price="R$ 35,00" 
      image="https://down-br.img.susercontent.com/file/sg-11134201-7rfgh-m9ronijvn6axe2@resize_w900_nl.webp"
      :inStock="true"
      @comprar="adicionarNaLista"
    />
    <UserCard 
      title="Espelho Led Abstrato" 
      price="R$ 284,41" 
      image="https://ae-pic-a1.aliexpress-media.com/kf/S8d73db854b29471287277d60bc1d8810v.jpg_720x720q75.jpg_.avif"
      :inStock="false"
      @comprar="adicionarNaLista"
    />
  </div>

</template>
