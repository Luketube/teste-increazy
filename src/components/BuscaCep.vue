<template>
<div>
    <input type="text" placeholder="Insira o CEP">
    <button type="reset"><img src="../assets/icone-plus.svg">Adicionar endereço</button>
</div>
    

</template>

<script>
export default{
    name: 'BuscaCep'
}

</script>

<style scoped>
div{
    align-items: center;
    display: flex;
    justify-content: space-between;
}
input{
    border: solid 2px #BBC4CE;
    border-radius: 8px;
    margin: 2rem 3rem 2rem 0;
    padding: 1rem;
    width: 300px;
}

button{
    background-color: #B600EE;
    border: none;
    border-radius: 8px;
    color: #FFFFFF;
    font-size: 16px;
    font-weight: 700;
    padding: 1rem;
    width: 300px;
}

button:hover{
    cursor: pointer;
}

img{
    align-items: center;
    margin-right: 1rem;
    max-width: 18px;
}

</style>