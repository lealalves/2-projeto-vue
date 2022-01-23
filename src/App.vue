<template>
    <div>
        <Header :esta_logado="false"/>
        <PrimeiroComponente/>
        <LifeCycle/>
        <Pessoa/>
    </div>
</template>

<script>
import PrimeiroComponente from "./components/PrimeiroComponente.vue"
import LifeCycle from "./components/LifeCycle.vue"
import Pessoa from "./components/Pessoa.vue"
import Header from "./components/Header.vue"


export default {
    name: 'App',
    components: {
        PrimeiroComponente,
        LifeCycle,
        Pessoa,
        Header
    }
}
</script>

<style>
    body{
        background-color: rgb(112, 112, 112);
        color: rgb(255, 255, 255);
    }
</style>