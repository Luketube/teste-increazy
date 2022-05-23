<template>
    <div>
        <input type="text" placeholder="Insira o CEP" pattern="[\d]{5}-?[\d]{3}">
        <button type="reset" @click="obtemCep"><img src="../assets/icone-plus.svg">Adicionar endereço</button>
    </div>

</template>

<script>

export default {
    name: 'BuscaCep',
    emits: ['aoEncontrarCep'],

    methods: {
        obtemCep() {
            const input = document.querySelector('input');
            const cep = input.value.replace(/\D/g, '');
            const url = `https://viacep.com.br/ws/${cep}/json/`;
            const options = {
                method: 'GET',
                mode: 'cors',
                headers: {
                    'content-type': 'application/json;charset=utf-8'
                }
            }
            if (!input.validity.patternMismatch && !input.validity.valueMissing) {
                fetch(url, options).then(
                    response => response.json()
                ).then(
                    data => {
                        if (data.erro) {
                            input.classList.add('invalido');
                            return;
                        }
                        input.setCustomValidity('');
                        input.classList.remove('invalido')
                        this.$emit('aoEncontrarCep', {
                            cep: data
                        })
                    }
                )
            } else {
                input.classList.add('invalido');
            }
        }
    }

}
</script>

<style scoped>
div {
    align-items: center;
    display: flex;
    justify-content: space-between;
}

input {
    border: solid 2px #BBC4CE;
    border-radius: 8px;
    margin: 2rem 3rem 2rem 0;
    padding: 1rem;
    width: 300px;
}

button {
    background-color: #B600EE;
    border: none;
    border-radius: 8px;
    color: #FFFFFF;
    font-size: 16px;
    font-weight: 700;
    padding: 1rem;
    width: 300px;
}

button:hover {
    cursor: pointer;
}

img {
    align-items: center;
    margin-right: 1rem;
    max-width: 18px;
}

.invalido {
    border-color: tomato;
}
</style>