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
        <div class="linha_vertical"></div>
        <button><img src="../assets/icone-lixo.svg" alt="Icone de lixeira"></button>
        
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
    padding: 1rem 0.5rem;
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
    padding: 1rem 1.5rem;
}

.linha_vertical{
    border: 1px solid #E0E6EA;
    height: 85px;
    margin-right: 0.5rem;
}

button{
    border: none;
    background-color: #FFFFFF;
}

button:hover{
    cursor: pointer;
}

</style>
