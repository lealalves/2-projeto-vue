<template>
    <div>
        <h1>Meu Formulário:</h1>
        <form @submit="enviarFormulario">
            Nome:
            <input type="text" v-model="name">
            <br>
            <br>
            E-mail:
            <input type="text" v-model="email">
            <br>
            <br>
            <InputSubmit/>
        </form>    
    </div>
</template>

<script>
import InputSubmit from "./form/Submit.vue"
import InputText from "./form/InputForm.vue"

export default {
    name: 'Form',
    components: {
        InputSubmit,
        InputText
    },
    data(){
        return {
            name: "",
            email: ""
        }
    },
    methods: {
        enviarFormulario (e) {
            e.preventDefault()

            const email = this.email
            const name = this.name


            console.log("enviado");
            console.log(email);
            console.log(name);
        }
    }
}
</script>