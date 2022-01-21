<template>
    <div>
        <h1>Olá Vue!</h1>
        <h2>Meu nome é {{ name }} e atualmente sou {{ profissao }}.</h2>
    </div>
</template>

<script>
export default {
    name: 'PrimeiroComponente',
    data(){
        return {
            name: 'Leal',
            profissao: 'estudante'
        }
    }
}
</script>