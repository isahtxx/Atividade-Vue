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

import UserCard from './components/ProductCard.vue'

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

        <UserCard 
        title="Almofada" 
        price="R$ 572,77" 
        image="https://http2.mlstatic.com/D_NQ_NP_2X_725176-MLA87652864645_072025-F.webp"
        :inStock="true"> 
    </UserCard>

</template>
