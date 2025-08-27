<script setup>
    const props = defineProps({
        title: String,
        price: String,
        image: String,
        inStock: Boolean,
    })

    const emit = defineEmits(["comprar"])

    function comprarProduto() {
    emit("comprar", props.title)
    }

</script>

<template>
    <div class="card" v-if="title">
        <h3>{{ title }}</h3>
        <p v-if="price">Preço: {{ price }}</p>
         <img :src="image" class="img" alt="..."></img>
        <div :class="inStock ? 'estoque' : 'esgotado'">{{ inStock ? 'Em estoque' : 'Esgotado' }}</div> <!-- classe do css - conteúdo a mostrar -->
        
        <div>
            <button @click="comprarProduto" :disabled="!inStock">Comprar</button>
        </div>
    </div>

</template>

<style scoped>
    .card{

        border: 1px solid #ccc;
        padding: 1rem;
        width: 325px;
        height: 310px;
        margin: 1rem;
    }

    .estoque{
        color:green
    }

    .esgotado{
        color: red
    }

    .img {
        width: 40%;
        border-radius: 6px;
    }

    button {
        background: #42b983;
        color: white;
        border: none;
        padding: 6px 12px;
        border-radius: 5px;
        cursor: pointer;
    }
    button:disabled {
        background: #ccc;
        cursor: not-allowed;
    }

</style>