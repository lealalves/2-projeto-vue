<template>
    <div>
        <p>{{email}} - {{email}}</p>
        <p v-if='esta_trabalhando'>Estou trabalhando no momento.</p>
        <p v-else>Não estou trabalhando.</p>
        <p>Utilizo as seguintes tecnologias para o back-end:</p>
        <ul>
            <li v-for="(tec, index) in backend_tec" :key="index">{{ tec }}</li>
        </ul>
        <p>Utilizo as seguintes tecnologias para o front-end</p>
        <ul>
            <li v-for="tec in frontend_tec" :key="tec.id">{{ tec.language }}</li>
        </ul>
        <div>
            <button @click="showEmail">{{ textoBotao }}</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para: {{email}}</p>
        <p>Para acessar meu portifólio <a v-bind:href="meu_link">basta clicar aqui</a></p>
        <Picture/>
    </div>
</template>
<script>

import Picture from "./Picture.vue"

export default {
    name: 'Info',
    components: {
        Picture
    },
    props: {
        email: String,
        esta_trabalhando: Boolean
    },
    data() {
        return {
            mostrar_email: false,
            meu_link: 'https://google.com',
            textoBotao: 'Mostrar E-mail',
            backend_tec: ['Javascript','PHP','Vue'],
            frontend_tec:[
                {id: 1, language: 'HTML'},
                {id: 2, language: 'CSS'},
                {id: 3, language: 'Vue'}
            ]
        }
    },
    methods: {
        showEmail () {
            this.mostrar_email = !this.mostrar_email
            if(!this.mostrar_email){
                this.textoBotao = 'Mostrar E-mail'
            }else{
                this.textoBotao = 'Ocultar E-mail'
            }
        }
    }
}
</script>