<template>
    <ul>
        <li><a href="">Home</a></li>
        <li><a href="">Projetos</a></li>
        <li><a href="">Contatos</a></li>
        <li v-if="esta_logado"><a href="#">Meu Perfil</a></li>
    </ul>
</template>

<script>
export default {
    name: 'Header',
    props: ['esta_logado']
}
</script>

<style scoped>
    ul{
        list-style: none;
        display: flex;
        background-color: black;
    }
    li{
        margin-right: 10px;
    }
    a{
        color: rgb(255, 0, 0);
        text-decoration: none;
        transition: .5s;
    }
    a:hover{
        color: royalblue;
    }
</style>