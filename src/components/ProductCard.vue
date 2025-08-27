<script setup>
    const props = defineProps({
        title: String,
        price: String,
        image: String,
        inStock: Boolean,
    })
</script>

<template>
    <div class="card" v-if="title">
        <h3>{{ title }}</h3>
        <p v-if="price">Preço: {{ price }}</p>
         <img :src="image" class="img" alt="..."></img>
        <div :class="inStock ? 'estoque' : 'esgotado'">{{ inStock ? 'Em estoque' : 'Esgotado' }}</div> <!-- classe do css - conteúdo a mostrar -->
    </div>

</template>

<style scoped>
    .card{
        border: 1px solid #ccc;
        padding: 1rem;
        margin: 1rem;
    }

    .estoque{
        color:green
    }

    .esgotado{
        color: red
    }

    .img{
        width: 30%;
    }

</style>