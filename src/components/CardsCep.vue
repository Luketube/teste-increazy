<template>
    <div class="card">
        <img src="../assets/icone-lugar.svg" alt="Icone de localização de mapas">
        <div class="card_conteudo">
            <div class="card_conteudo_celular">
                <p class="nome_rua">{{ arrayCeps[posicao].cep.logradouro }}</p>
                <p>{{ arrayCeps[posicao].cep.localidade }} - {{ arrayCeps[posicao].cep.uf }}</p>
            </div>
            <p class="cep">{{ arrayCeps[posicao].cep.cep }}</p>
        </div>
        <div class="linha_vertical"></div>
        <button @click="excluiCard"><img src="../assets/icone-lixo.svg" alt="Icone de lixeira"></button>
    </div>

</template>

<script>
export default {
    name: 'CardsCep',
    props: {
        arrayCeps: {
            type: Object
        },
        posicao: {
            type: Number
        }
    },
    emits:['cardRemovido'],
    methods: {
        excluiCard(){
            this.$emit('cardRemovido', {
                posicao: this.posicao
            })
        }
    }
}

</script>

<style scoped>
.card {
    align-items: center;
    border-radius: 8px;
    box-shadow: 5px 10px 25px 0px #888888;
    display: flex;
    margin-top: 3rem;
    padding: 1rem 0.5rem;
}

img {
    margin: .5rem;
    max-width: 20px;
}

.card_conteudo {
    align-items: center;
    display: flex;
    justify-content: space-between;
    width: 100%;

}

.nome_rua {
    font-weight: 800;
    font-size: 1.3rem;
    margin-bottom: .5rem;
    width: max-content;
}

.cep {
    color: #B600EE;
    padding: 1rem 1.5rem;
}

.linha_vertical {
    border: 1px solid #E0E6EA;
    height: 85px;
    margin-right: 0.5rem;
}

button {
    border: none;
    background-color: #FFFFFF;
}

button:hover {
    cursor: pointer;
}

@media only screen and (max-width: 375px) {
    .card {
        flex-direction: column;
    }
    .card_conteudo{
        flex-direction: column;
    }

    .linha_vertical {
        height: 1px;
        width: 255px;
        margin-bottom: 1rem;
    }
}
</style>
