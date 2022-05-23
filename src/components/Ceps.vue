<template>
    <ul>
        <li>
            <img src="../assets/icone-lugar.svg" alt="Icone de marcação de mapa">
            <p><strong>CEP</strong>{{ cep.cep }}</p>
        </li>
    </ul>

</template>

<script>

export default{
    name: 'ListaCeps',
    props:{
        cep: {
            type: Object
        }
    }
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

</style>