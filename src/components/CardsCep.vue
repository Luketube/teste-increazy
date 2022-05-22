<template>
    <div class="card">
        <img src="../assets/icone-lugar.svg" alt="Icone de localização de mapas">
        <div class="card_conteudo">
            <div>
            <p class="nome_rua">Rua Luiz Briski</p>
            <p>Vinhedo - SP</p>
            </div>
            <p class="cep">13284-054</p>    
        </div>
        <img src="../assets/icone-lixo.svg" alt="Icone de lixeira">
    </div>

</template>

<script>
export default{
    name: 'CardsCep'
}

</script>

<style scoped>
.card{
    align-items: center;
    border-radius: 8px;
    box-shadow: 5px 10px 25px 0px #888888;
    display: flex;
    margin-top: 3rem;
    padding: 2rem 0.5rem;
}

img{
    margin: .5rem;
    max-width: 20px;
}

.card_conteudo{
    align-items: center;
    display: flex;
    justify-content: space-between;
    width: 100%;

}

.nome_rua{
    font-weight: 800;
    font-size: 1.3rem;
    margin-bottom: .5rem;
    width: max-content;
}

.cep{
    color: #B600EE;
    border-right: 1px solid #E0E6EA;
    padding: 1rem 1.5rem;
    margin-right: 0.5rem;
}

</style>
