<template>
    <div>
        <h1>Olá Vue!</h1>
        <h2>Meu nome é {{ name }} e atualmente sou {{ profissao }}.</h2>
        <MultiplosEventos />
    </div>
</template>

<script>
import MultiplosEventos from "./MultiplosEventos.vue"


export default {
    name: 'PrimeiroComponente',
    components: {
        MultiplosEventos
    },
    data(){
        return {
            name: 'Leal',
            profissao: 'estudante'
        }
    }
}
</script>