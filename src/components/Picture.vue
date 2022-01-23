<template>
    <div>
        <img :src="avatar" :alt="descricao">
        <MudarImagem @trocar-img="trocarImagem" />
    </div>
</template>

<script>
import MudarImagem from "./MudarImagem.vue"

export default {
    name: 'Picture',
    components: {
        MudarImagem
    },
    data(){
        return {
            avatar: '/img/avatar.png',
            descricao: 'Vinicius Leal'
        }
    },
    methods: {
        trocarImagem() {
            this.avatar = 'img/avatar2.png'
        }
    }
}
</script>