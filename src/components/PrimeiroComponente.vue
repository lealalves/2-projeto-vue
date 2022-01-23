<template>
    <div>
        <Reutilizacao />
        <h1>Olá Vue!</h1>
        <Reutilizacao />
        <h2>Meu nome é {{ name }} e atualmente sou {{ profissao }}.</h2>
        <MultiplosEventos />
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
        <Reutilizacao />
    </div>
</template>

<script>
import MultiplosEventos from "./MultiplosEventos.vue"
import Reutilizacao from "./Reutilizacao.vue"

export default {
    name: 'PrimeiroComponente',
    components: {
        MultiplosEventos,
        Reutilizacao
    },
    data(){
        return {
            name: 'Leal',
            profissao: 'estudante'
        }
    }
}
</script>