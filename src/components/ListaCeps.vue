<template>
    <ul>
        <li>
            <img src="../assets/icone-lugar.svg" alt="Icone de marcação de mapa">
            <p><strong>CEP</strong>13284-054</p>
        </li>
    </ul>

    <div class="botao">
        <button>Gerar Endereços</button>
    </div>

    <hr>

</template>

<script>
export default{
    name: 'ListaCeps'
}

</script>

<style scoped>
ul{
    margin-top: 2rem;
}

li{
    align-items: center;
    display: flex;
    font-size: 1.2rem;
}

img{
    margin-right: 1rem;
}

p{
    font-weight: 600;
    color: #BBC4CE;
}

strong{
    color: #333333;
    font-weight: bold;
    margin-right: .5rem;
}

.botao{
    display: flex;
    justify-content: flex-end;

}

button{
    background-color: #B600EE;
    border: none;
    border-radius: 8px;
    color: #FFFFFF;
    font-size: 16px;
    font-weight: 700;
    margin: 3rem 0;
    padding: 1rem;
    width: 300px;
}

</style>