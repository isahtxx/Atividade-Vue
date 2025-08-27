<script setup>
    let text = '<p style="color: red;">Texto em vermelho</p>'
    let texto = '<strong>Texto</strong>'
</script>

<template>
    <div v-html="text"></div> <!-- aparece em vermelho -->
    <div>{{ text }}</div>

    <div v-html="texto"></div> <!-- aparece em negrito -->
    <div>{{ texto }}</div>

</template>