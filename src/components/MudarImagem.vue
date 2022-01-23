<template>
    <div>
        <button @click="$emit('trocarImg')">Mudar Imagem</button>
    </div>
</template>

<script>
export default {
    name: 'MudarImagem',
    emits: ['trocarImg']
}
</script>