<template>
    <h1>Meu nome é: {{ nome }}</h1>
</template>

<script>
export default {
    name: 'LifeCycle',
    data(){
        return {
            nome: 'Ainda não sei'
        }
    },
    created(){
        setTimeout(() =>{
            this.nome = 'Leal'
        },1000)
        this.LifeCycle()
    },
    mounted() {
        setTimeout(() =>{
            this.nome = 'Alves'
        },2000)
        this.LifeCycle()
    },
    methods: {
        LifeCycle () {
            console.log('Executouuuuu');
        }
    }
}
</script>