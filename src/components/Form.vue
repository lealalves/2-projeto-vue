<template>
    <div>
        <h1>Meu Formulário:</h1>
        <form action="">
            Nome:
            <InputText/>
            <br>
            <br>
            Idade:
            <InputText/>
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
    }
}
</script>